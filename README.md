# MyaLphabet.app – School Information Management System

MyaLphabet.app is a comprehensive school information management platform designed by and for aLphabet internationaL schooL. It helps manage attendance, timetables, cafeteria menus, calendar events, house point systems, and more — all through a centralized web dashboard.

---

## Features

### Core Modules
- **Attendance Management**: Track, view, and report attendance by grade-section.
- **Timetable System**: Interactive grade-wise, teacher-wise, and room-wise scheduling with subject mappings.
- **School & Class Calendar**: Manage events at school and classroom levels. Supports recurring/multi-day events.
- **House Point Management**: Assign students to houses and track behavior or achievement-based points.
- **Cafeteria Menu Planner**: Design weekly menus, create dishes, and gather feedback through a rating system.

### Dashboard Overview
- View quick stats: Attendance %, upcoming events, menu of the day, leaderboard (house points), and recent updates.
- Fully role-based views for Admin, Teacher, and Student.

### Roles & Access Levels
- **Admin**: Full access to all modules and configurations.
- **Teacher**: Access to class-specific attendance, timetables, calendar events, and reports.
- **Student**: View only access to personal data (timetable, attendance, house points, menus).

---

## Tech Stack

| Layer         | Tech                         |
|---------------|------------------------------|
| Frontend      | React.js + Tailwind CSS + Axios |
| Backend       | Node.js + Express.js         |
| ORM           | Prisma                       |
| Database      | PostgreSQL                   |
| Auth          | JWT-based Authentication     |
| Deployment    | Docker + Nginx (optional)    |

---

## 📁 Project Structure

myalphabet-app/
├── backend/
│ ├── src/
│ │ ├── prisma/ # Prisma schema & migrations
│ │ ├── routes/ # API routes (attendance, calendar, etc.)
│ │ ├── controllers/ # Business logic per module
│ │ ├── middleware/ # Auth and error handling
│ │ └── app.ts # Express server setup
├── frontend/
│ ├── src/
│ │ ├── pages/ # React pages by module
│ │ ├── components/ # Shared components (navbar, sidebar, etc.)
│ │ └── utils/api.ts # Axios API wrapper



## API Overview

| Method | Endpoint                       | Description                    |
|--------|--------------------------------|--------------------------------|
| POST   | `/api/auth/login`              | User login                     |
| GET    | `/api/attendance/my-attendance`| Fetch logged-in user's attendance |
| POST   | `/api/attendance/mark`         | Mark attendance (admin/teacher)|
| GET    | `/api/calendar/school`         | Get school events              |
| POST   | `/api/calendar/class`          | Add/edit class calendar events |
| GET    | `/api/house/points`            | View house leaderboard         |
| POST   | `/api/menu/create`             | Create weekly menu             |
| GET    | `/api/menu/this-week`          | Get menu for the current week  |

> Full API documentation is available in the `/docs` directory.

---

## UI Sketches (Figma)

- Text-based UI sketches and master wireframe flow are available in documentation.
- Includes side menu layouts, dashboards, and module-specific page layouts.

---

## Setup Instructions

### 1. Clone the Repository

`bash
git clone https://github.com/your-org/myalphabet-app.git
cd myalphabet-app`


### 2. Backend Setup

`bash 
cd backend
cp .env.example .env
npm install
npx prisma generate
npx prisma migrate dev --name init
npm run dev`

### 3. Frontend Setup

`bash
cd frontend
npm install
npm start
Development Progress
Prisma schema created`

 Boilerplate backend and frontend integrated

Module UI wireframes prepared

Unit tests and CI/CD pipeline

Mobile view optimization

📄 License
This project is licensed under the IT Dept - aLphabet internationaL schooL© 2025.



