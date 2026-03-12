# Hospital Santa Joana - Hospital Management System

<p align="center">
  <img src="client/img/hsj_logo.png" alt="Hospital Santa Joana logo" width="220">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Java-17-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java 17">
  <img src="https://img.shields.io/badge/Spring_Boot-3.x-6DB33F?style=for-the-badge&logo=springboot&logoColor=white" alt="Spring Boot">
  <img src="https://img.shields.io/badge/MySQL-8-4479A1?style=for-the-badge&logo=mysql&logoColor=white" alt="MySQL">
  <img src="https://img.shields.io/badge/React-Admin-61DAFB?style=for-the-badge&logo=react&logoColor=0B1D2A" alt="React Admin">
  <img src="https://img.shields.io/badge/JavaScript-Frontend-F7DF1E?style=for-the-badge&logo=javascript&logoColor=111111" alt="JavaScript Frontend">
  <img src="https://img.shields.io/badge/Docker-Compose-2496ED?style=for-the-badge&logo=docker&logoColor=white" alt="Docker Compose">
</p>

## 🎬 Media Gallery

### Screenshots

![Overview](media/overview.png)
![Login screen](media/login%20screen.png)
![Order placed](media/order_placed.png)
![Invoice](media/invoice.png)
![Admin overview](media/admin_overview.png)
![Admin products](media/admin_products.png)
![Admin rooms](media/admin_rooms.png)

### Videos

- [Client flow video](media/cliente%20flow.mp4)
- [Admin flow video](media/admin%20flow.mp4)

Welcome to the Hospital Santa Joana hospital management system repository! This project offers a comprehensive solution for patient management, meal orders, invoices, rooms, and much more, with a modern web frontend and robust backend.

---

## ✨ Overview

- **Frontend:** Responsive SPA for patients, with meal orders, history, invoices, and profile.
- **Backend:** RESTful API in Java Spring Boot, MySQL persistence.
- **Admin:** Administrative panel (React) for managing products, categories, rooms, patients, etc.
- **Infrastructure:** Docker Compose for container orchestration.

---

## 🚀 Quick Start

### 1. Clone the repository
```bash
git clone https://github.com/MigueldsBatista/projeto_database.git
cd projeto_database
```

### 2. Start the backend (API + database)
```bash
cd santajoana
# Edit compose.yaml if you want to customize ports
sudo docker compose up -d
```
Wait until the backend is available at http://localhost:8080

### 3. Populate the database
```bash
mysql -h 127.0.0.1 -P 3307 -u admin -p < populate_database.sql
```
Or use a graphical client (DBeaver, MySQL Workbench, etc) and run the `populate_database.sql` script.

### 4. Start the frontend
- **Via Live Server (VS Code):**
  1. Open the `client/` folder in VS Code
  2. Right-click on `index.html` > "Open with Live Server"
  3. Access `http://127.0.0.1:5500/index.html`
- **Via Docker/Nginx:**
  1. Adjust `nginx.conf` if necessary
  2. Run the container according to Dockerfile instructions

---

## ⚙️ Detailed Configuration

### Prerequisites
- Docker and Docker Compose
- MySQL Client (to populate database)
- Visual Studio Code + Live Server (optional, for frontend)

### Backend
- The backend starts via Docker Compose and exposes the API at `http://localhost:8080`.
- The MySQL database runs on `localhost:3307` (see compose.yaml).
- The `populate_database.sql` script inserts essential data (categories, products, patients, rooms, etc).

### Frontend
- The frontend expects the API at `http://localhost:8080` (adjust in `js/utils.js` if necessary).
- Use Live Server or a static web server to run the interface.

### Admin
- The admin panel runs in React (folder `admin/`).
- Install dependencies and run with:
```bash
cd admin
npm install
npm start
```

<p align="center">
  <img src="client/img/hsj_logo.png" alt="Hospital Santa Joana logo" width="160">
</p>

---

## 🧩 Features
- Patient registration and login
- Meal ordering by category
- Shopping cart
- Order history and details
- Invoice viewing and payment status
- Patient profile
- Admin panel for managing products, categories, rooms, patients, invoices, etc

