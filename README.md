# Task Management System - Frontend Dashboard

## Overview
The Frontend Dashboard is a Laravel 10 web application that consumes APIs to manage tasks. It provides an interactive dashboard built with Blade and TailwindCSS, allowing users to view tasks grouped by status (Pending, In Progress, Completed).  

**Note:** Authentication is shared via Laravel Breeze, but this project uses **API calls with Sanctum tokens** to fetch and manage data.  

**Important:** If running both frontend and backend on the same machine, you may need to change the Laravel server port (`APP_URL`) and database port (`DB_PORT`) to avoid conflicts.

---

## Features
- Login and registration (Laravel Breeze)
- View tasks grouped by status
- Add, edit, delete, and mark tasks as completed via API
- Assign users to tasks and remove assignees via API
- Comment system for tasks with chronological history via API
- Postpone tasks with reason and history via API
- Real-time search and filtering by title, description, status, and priority
- Kanban board for task organization
- Interactive charts: Doughnut (task status), Bar (priority counts)
- Highlight tasks based on priority (High, Medium, Low)
- Notifications for tasks due soon
- SweetAlert confirmation popups
- Responsive UI with TailwindCSS

---

## Technology Stack
| Component        | Technology / Version |
|-----------------|--------------------|
| Backend          | Laravel 10+        |
| PHP              | 8.1+               |
| Database         | MySQL 8.x          |
| Frontend         | Blade Templates, TailwindCSS 3.x |
| Authentication   | Laravel Breeze     |
| API Protection   | Laravel Sanctum 3.3 |
| JavaScript       | Alpine.js          |
| Node.js & NPM    | Node.js 18+, NPM 9+ |
| Other Tools      | Composer 2.x, SweetAlert |
| Version Control  | Git / GitHub       |

---

## Installation Instructions
1. Clone or unzip the project into your web server root, e.g., `C:\xampp\htdocs\frontend-dashboard`.
2. Configure the `.env` file to connect to the **same database as the backend**. If the database is using a **different port**, update `DB_PORT` (e.g., `3307`).
3. Start XAMPP (Apache + MySQL). If using a custom port, update `.env` `APP_URL=http://localhost:8001`.
4. Install PHP dependencies: `composer install`
5. Install Node.js dependencies: `npm install`
6. Run migrations (if needed for local tables): `php artisan migrate`
7. Start Laravel server on port 8001: `php artisan serve --port=8001`
8. Compile frontend assets: `npm run dev`

---

## API Endpoints (Consumed)
All endpoints are accessed using **Bearer token** from Sanctum authentication:

- `GET /api/tasks` – Fetch tasks with filters (search, status, priority)
- `POST /api/tasks` – Create a task
- `PUT /api/tasks/{id}` – Update a task
- `DELETE /api/tasks/{id}` – Delete a task
- `POST /api/tasks/{id}/complete` – Mark a task as completed
- `POST /api/tasks/{id}/postpone` – Postpone a task
- `POST /api/tasks/{id}/comments` – Add a comment
- `POST /api/tasks/{id}/assign` – Assign users
- `POST /api/tasks/{id}/remove-members` – Remove users
- `GET /api/dashboard-data` – Fetch dashboard statistics

---

## Deliverables
- Fully functional Frontend Dashboard project
- API integration with backend for task management
- Postman collection for API testing (available in repository)
- README.md with installation and setup instructions
- Screenshots or demo showing task notifications and interactive charts

---

## Author
Developed by: M.F.F. Infaza  
Date: 19th September 2025

