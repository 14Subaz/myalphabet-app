Architecture Overview - MyaLphabet.app

Architecture Style: Microservices


Type: Desktop-optimized Web App


API Style: REST


Authentication: JWT-based Token Authentication


Interconnectivity: All modules interlinked via secure APIs and shared data models




1. Frontend - Client Side
Layer
Technology
Purpose
Framework
React.js
Fast, modular, and scalable UI for dashboards and modules
State Management
Redux Toolkit + React Query
Manage global state and server state efficiently
Styling
Tailwind CSS + ShadCN UI
Consistent, responsive, customizable design system
Routing
React Router DOM
Module-based and nested routing
Charting
Recharts or Chart.js
Display analytics (attendance stats, house points, etc.)
Form Handling
React Hook Form + Yup
Forms for attendance, events, ratings, etc.
Calendar Views
FullCalendar or React Big Calendar
For calendar UI in class and school calendar modules








2. Backend - Server Side APIs
Layer
Technology
Purpose
Framework
.NET 7+ (ASP.NET Core Web API)
Robust, secure, scalable RESTful API service
Authentication
Identity + JWT
User login, roles, secure endpoints
ORM
Entity Framework Core
Database mapping and migration
Caching
Redis 
Performance boost for timetable & dashboard queries
Email/Notifications
MailKit or SendGrid
Notification for point updates, reminders, alerts
File Upload/Export
iTextSharp
For attendance PDF/Excel exports


3. Database - Persistence Layer
Component
Technology
Purpose
Relational DB
MS SQL Server
Structured storage of all school data
NoSQL 
MongoDB 
Store logs, menu ratings, dashboard cache, etc.
Blob/File Storage
Azure Blob / AWS S3 / Local File System
Store reports, attachments, student photos


4. Security
Feature
Tech
Details
Authentication
JWT
Secure access tokens
Authorization
Role-Based Access Control
Roles: Super Admin, Admin, Teacher, Student
Audit Logs
Custom Middleware
Track logins, updates, deletions
HTTPS
TLS
Enforced across entire application
Rate Limiting
Middleware (e.g., AspNetCoreRateLimit)
Prevent brute-force attacks

5. DevOps & Hosting
Layer
Tech Stack
Purpose
Source Control
Git + GitHub/GitLab
Version control & CI/CD
CI/CD
GitHub Actions / Azure DevOps
Build, test, deploy
Containerization
Docker
For consistent deployment
Web Hosting
Azure App Service / IIS / AWS EC2
Host backend APIs
Frontend Hosting
Azure Static Web Apps / Vercel / Netlify
Deploy frontend
Monitoring
Azure Monitor / Application Insights
Track performance & errors


6. Predictable Tools
Tool
Use Case
Swagger / Swashbuckle
Auto-generate API documentation
Postman Collection
API testing and documentation
Power BI (future)
Deeper school analytics on attendance, points, etc.
SignalR (future)
Real-time updates for attendance/notifications


Future Expansion
PWA (Progressive Web App) for mobile-like experience


GraphQL API Gateway for better frontend querying


Multilingual Support using i18n


Role-based dashboard widgets visibility

