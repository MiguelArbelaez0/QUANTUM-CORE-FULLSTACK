# Quantum Core

> Sistema web integral para la gestión de transacciones financieras, desarrollado con React, Flask, Prisma, MySQL y Docker.

Quantum Core es una aplicación web desarrollada como proyecto académico para gestionar y analizar transacciones financieras mediante una arquitectura cliente-servidor.

El proyecto integra un interfaz en React, una API REST desarrollada con Python y Flask, Prisma ORM y una base de datos MySQL ejecutada mediante Docker.

## 📌 Descripción general

Quantum Core permite realizar un flujo completo de gestión de transacciones:

- Crear, consultar, actualizar y eliminar registros.
- Calcular estadísticas financieras.
- Calcular el saldo neto.
- Validar los datos de entrada.
- Consumir una API REST.
- Persistir información en MySQL.
- Utilizar una interfaz web adaptable.

Flujo principal:

```text
Usuario
  ↓
React + Vite
  ↓
HTTP / JSON
  ↓
API REST con Flask
  ↓
Prisma ORM
  ↓
MySQL
```

## 🏗️ Arquitectura

La aplicación separa la presentación, la API, la lógica de aplicación y la persistencia.

```text
Frontend
React + Vite
     │
     │ HTTP / JSON
     ▼
Backend
Python + Flask
     │
     ▼
Prisma ORM
     │
     ▼
Base de datos
MySQL 8
     │
     ▼
Docker
```

Esta estructura mantiene las responsabilidades separadas y facilita el mantenimiento del proyecto.

## 🚀 Funcionalidades

- Crear transacciones.
- Consultar transacciones.
- Consultar una transacción individual.
- Actualizar transacciones.
- Eliminar transacciones.
- Calcular ingresos totales.
- Calcular egresos totales.
- Calcular saldo neto.
- Mostrar estadísticas financieras.
- Validar datos de las transacciones.
- Mostrar mensajes de éxito y error.
- Consumir la API REST desde React.
- Persistir información en MySQL.
- Interfaz web adaptable.

## 💰 Gestión de transacciones

Las operaciones CRUD se realizan mediante la API REST.

| Operación | Método HTTP | Propósito |
|---|---|---|
| Crear | POST | Registrar una transacción |
| Consultar | GET | Obtener transacciones |
| Actualizar | PUT | Modificar una transacción |
| Eliminar | DELETE | Eliminar una transacción |

El interfaz no accede directamente a la base de datos. Todas las operaciones pasan por la API desarrollada con Flask.

## 📊 Estadísticas financieras

La aplicación calcula información a partir de las transacciones almacenadas:

- Total de transacciones.
- Total de ingresos.
- Total de egresos.
- Saldo neto.

El saldo neto se calcula como:

```text
SALDO NETO = INGRESOS - EGRESOS
```

## 🌐 API REST

La API principal se encuentra bajo:

```text
/api/transacciones/
```

Operaciones disponibles:

```text
GET     /api/transacciones/
GET     /api/transacciones/<id>
POST    /api/transacciones/
PUT     /api/transacciones/<id>
DELETE  /api/transacciones/<id>
```

La comunicación entre React y Flask utiliza HTTP y JSON.

## 🧩 Tecnologías

| Tecnología | Uso |
|---|---|
| React | Interfaz web |
| Vite | Herramientas y servidor de desarrollo |
| JavaScript | Lenguaje del interfaz |
| Tailwind CSS | Estilos de la interfaz |
| Fetch API | Comunicación HTTP |
| Python | Lenguaje del servidor |
| Flask | Desarrollo de la API REST |
| Flask-CORS | Comunicación entre orígenes |
| Prisma ORM | Acceso a datos |
| MySQL 8 | Base de datos relacional |
| Docker | Contenerización de la base de datos |

## 🗄️ Persistencia

Prisma ORM funciona como capa de acceso entre Flask y MySQL.

MySQL se ejecuta mediante Docker, proporcionando un entorno local reproducible para el desarrollo.

La configuración de la base de datos se carga mediante variables de entorno. Las credenciales sensibles deben permanecer únicamente en el entorno local.

## 🖥️ Interfaz

La interfaz está desarrollada con React y Vite e incluye:

- Gestión de transacciones.
- Estadísticas financieras.
- Formularios de transacciones.
- Edición y eliminación.
- Validación de datos.
- Mensajes de éxito y error.
- Diseño adaptable.

## 📂 Estructura principal

```text
QUANTUM-CORE-FULLSTACK/
│
├── Proyecto_Completo/
│   ├── BACKEND/
│   │   ├── controllers/
│   │   ├── models/
│   │   ├── routes/
│   │   ├── db.py
│   │   └── app.py
│   │
│   └── FRONTEND/
│       └── Aplicación React + Vite
│
└── README.md
```

## ⚙️ Instalación

### 1. Clonar el repositorio

```bash
git clone https://github.com/MiguelArbelaez0/QUANTUM-CORE-FULLSTACK.git
cd QUANTUM-CORE-FULLSTACK
```

### 2. Base de datos

Iniciar el contenedor de MySQL utilizado por el proyecto:

```bash
docker start empresa
```

### 3. Servidor

Desde la carpeta del servidor, activar el entorno de Python e iniciar la API:

```powershell
cd Proyecto_Completo\BACKEND
.\.venv\Scripts\Activate.ps1
python app.py
```

El servidor utiliza el puerto `5000`.

### 4. Interfaz

Desde la carpeta del interfaz:

```bash
cd Proyecto_Completo/FRONTEND
npm install
npm run dev
```

El servidor de desarrollo de Vite utiliza el puerto `5173`.

> Mantén los archivos como `.env` únicamente en local. Nunca publiques contraseñas ni credenciales sensibles.

## ▶️ Acceso local

**Interfaz**
```text
http://localhost:5173
```

**Servidor**
```text
http://127.0.0.1:5000
```

**API**
```text
http://127.0.0.1:5000/api/transacciones/
```

## 🎯 Qué demuestra este proyecto

- Desarrollo web integral.
- React y Vite.
- Python y Flask.
- Diseño de APIs REST.
- Prisma ORM.
- MySQL.
- Docker.
- Operaciones CRUD.
- Arquitectura cliente-servidor.
- Validación de datos.
- Agregación de información financiera.
- Integración entre interfaz y servidor.
- Diseño de interfaces adaptables.
- Separación de responsabilidades.

## 📌 Estado del proyecto

**Proyecto académico y de portafolio terminado.**

## 👨‍💻 Autor

**Miguel Arbeláez Vallejo**

Desarrollador de Software | Flutter y Dart | Desarrollo integral | Servidor | IA y Datos

- GitHub: https://github.com/MiguelArbelaez0
- LinkedIn: https://www.linkedin.com/in/miguel-arbelaez-v-57719542b/
