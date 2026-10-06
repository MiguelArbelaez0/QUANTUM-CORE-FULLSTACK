# Quantum Core

> Full-Stack transaction management system built with React, Flask, Prisma and MySQL.

Quantum Core is a full-stack web application developed as an academic project for managing and analyzing financial transactions through a client-server architecture.

The project demonstrates the integration of a React frontend, a Python Flask REST API, Prisma ORM, and a MySQL database running through Docker.

## 📌 Overview

Quantum Core provides a complete transaction-management workflow with:

- Create, read, update, and delete operations.
- Financial statistics and aggregation.
- Net balance calculation.
- Input validation.
- REST API communication.
- Persistent storage with MySQL.
- Responsive web interface.

The main application flow is:

```text
User
  ↓
React + Vite
  ↓
HTTP / JSON
  ↓
Flask REST API
  ↓
Prisma ORM
  ↓
MySQL
```

## 🏗️ Architecture

The application separates the presentation layer, backend API, business operations, and data persistence.

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
Database
MySQL 8
     │
     ▼
Docker
```

This structure keeps the frontend, API layer, and persistence layer independent and easier to maintain.

## 🚀 Features

- Create financial transactions.
- View transaction records.
- View individual transactions.
- Update transactions.
- Delete transactions.
- Calculate total credits.
- Calculate total debits.
- Calculate net balance.
- Display financial statistics.
- Validate transaction data.
- Provide success and error feedback.
- Consume a REST API from the frontend.
- Persist data in MySQL.
- Responsive web interface.

## 💰 Transaction Management

The application implements CRUD operations through the REST API.

| Operation | HTTP method | Purpose |
|---|---|---|
| Create | POST | Register a transaction |
| Read | GET | Retrieve transactions |
| Update | PUT | Modify a transaction |
| Delete | DELETE | Remove a transaction |

The frontend does not access the database directly. All transaction operations pass through the Flask API.

## 📊 Financial Statistics

The application calculates financial information from the stored transaction data.

The main indicators are:

- Total transactions.
- Total credits.
- Total debits.
- Net balance.

The net balance is calculated as:

```text
NET BALANCE = CREDITS - DEBITS
```

This demonstrates data aggregation and business-oriented calculations in a full-stack application.

## 🌐 REST API

The Flask backend exposes the transaction API under:

```text
/api/transacciones/
```

The available operations include:

```text
GET     /api/transacciones/
GET     /api/transacciones/<id>
POST    /api/transacciones/
PUT     /api/transacciones/<id>
DELETE  /api/transacciones/<id>
```

Communication between the React frontend and Flask backend uses HTTP and JSON.

## 🧩 Technologies

| Technology | Usage |
|---|---|
| React | Frontend application |
| Vite | Frontend tooling and development server |
| JavaScript | Frontend programming language |
| Tailwind CSS | Interface styling |
| Fetch API | HTTP communication |
| Python | Backend programming language |
| Flask | REST API framework |
| Flask-CORS | Cross-origin communication |
| Prisma ORM | Database access |
| MySQL 8 | Relational database |
| Docker | Database containerization |

## 🗄️ Persistence

Prisma ORM is used as the data-access layer between the Flask backend and MySQL.

MySQL runs through Docker, providing a reproducible local database environment for development.

The backend loads database configuration through environment variables. Sensitive configuration should remain local and must not be committed to the repository.

## 🖥️ Interface

The frontend is built with React and Vite and provides:

- Transaction management views.
- Financial statistics.
- Transaction forms.
- Edit and delete interactions.
- Validation feedback.
- Success and error messages.
- Responsive layout.

## 📂 Project Structure

The main application is contained inside the `Proyecto_Completo` directory:

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
│       └── React + Vite application
│
└── README.md
```

The backend contains the Flask API, controllers, routes, Prisma integration, and database configuration. The frontend contains the React application and user interface.

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/MiguelArbelaez0/QUANTUM-CORE-FULLSTACK.git
cd QUANTUM-CORE-FULLSTACK
```

### 2. Database

Start the MySQL Docker container used by the project:

```bash
docker start empresa
```

The local environment uses MySQL through Docker rather than requiring a separate local MySQL installation.

### 3. Backend

From the backend directory, activate the Python environment and start the Flask API:

```powershell
cd Proyecto_Completo\BACKEND
.\.venv\Scripts\Activate.ps1
python app.py
```

The backend runs on port `5000`.

### 4. Frontend

From the frontend directory:

```bash
cd Proyecto_Completo/FRONTEND
npm install
npm run dev
```

The Vite development server runs on port `5173`.

> Keep environment files such as `.env` local. Never commit database passwords or other sensitive credentials.

## ▶️ Local Access

### Frontend

```text
http://localhost:5173
```

### Backend

```text
http://127.0.0.1:5000
```

### API

```text
http://127.0.0.1:5000/api/transacciones/
```

## 🔄 Application Flow

```text
User
  ↓
React Interface
  ↓
Fetch API
  ↓
Flask REST API
  ↓
Controllers / Routes
  ↓
Prisma ORM
  ↓
MySQL
```

The frontend handles user interaction, the Flask API processes requests, the backend routes requests through the application logic, Prisma manages database access, and MySQL provides persistent storage.

## 🎯 What This Project Demonstrates

This project demonstrates practical experience with:

- Full-stack web development.
- React and Vite.
- Python and Flask.
- REST API development.
- Prisma ORM.
- MySQL.
- Docker.
- CRUD operations.
- Client-server architecture.
- Data validation.
- Financial data aggregation.
- REST-based frontend/backend integration.
- Responsive web interfaces.
- Separation of application responsibilities.

## 📌 Project Status

**Completed academic and portfolio project.**

The project was developed to demonstrate practical full-stack development, REST API design, database integration, Docker-based persistence, and client-server architecture.

## 👨‍💻 Author

**Miguel Arbeláez Vallejo**

Software Developer | Flutter & Dart | Full-Stack | Backend | AI/Data

- GitHub: https://github.com/MiguelArbelaez0
- LinkedIn: https://www.linkedin.com/in/miguel-arbelaez-v-57719542b/
