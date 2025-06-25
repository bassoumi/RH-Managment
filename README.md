🏢 HR Management Application

Streamline HR processes with a full‑stack solution powered by Angular, Django, and MySQL.
Modern UI for employees · Powerful admin tools for HR teams.





✨ Key Features

👩‍💼 Admin Interface

Employee Management – Create, edit, and archive employee profiles.

Training Sessions – Plan, assign, and monitor completion.

Leave Requests – Approve or reject with one click (auto‑email notifications).

Analytics Dashboard – Attendance, leave trends, and training KPIs in real‑time charts.

👨‍💻 Employee Portal

Secure Login – First‑time password reset enforced.

Training Catalog – Browse sessions and self‑enroll.

Leave Management – Request leave, upload proof, track status live.

Self‑Service – Update personal details and manage credentials.

🏗️ Tech Stack

Layer

Tech / Tools

Frontend

Angular 17 · RxJS · Tailwind

Backend

Django 5 · Django REST Framework

Database

MySQL 8 (switchable to PostgreSQL)

Auth

JSON Web Tokens (JWT)

DevOps

Docker · GitHub Actions · Pre‑commit

Languages in this repo: TypeScript (Angular) · Python (Django) · HTML/SCSS · SQL

📂 Project Structure

HR‑Management‑App/
 ├─ hr_backend/        # Django project (REST API)
 └─ hr_frontend/       # Angular app (SPA)

🚀 Quick Start

Prerequisites

Tool

Minimum Version

Node.js

18 LTS

Angular CLI

17

Python

3.11

pip / Poetry

23

MySQL Server

8

Docker (optional)

24

1️⃣ Clone the repo

git clone https://github.com/bassoumi/HR-Management-App.git
cd HR-Management-App

2️⃣ Backend setup (Django)

cd hr_backend
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env           # configure DB, SECRET_KEY, JWT settings
python manage.py migrate
python manage.py runserver     # API on http://localhost:8000

3️⃣ Frontend setup (Angular)

cd ../hr_frontend
npm install -g @angular/cli   # if needed
npm install
ng serve --open               # SPA on http://localhost:4200

🌐 URLs

URL

Description

http://localhost:4200

Employee portal

http://localhost:4200/admin

HR admin UI

http://localhost:8000/api

REST API root

http://localhost:8000/api/docs

Swagger / Redoc

⚙️ Environment Variables

Backend .env example:

DJANGO_SECRET_KEY=super-secret
DB_NAME=hrdb
DB_USER=root
DB_PASSWORD=pass
DB_HOST=localhost
DB_PORT=3306

Frontend environment.ts snippet:

export const environment = {
  production: false,
  apiUrl: 'http://localhost:8000/api',
};

🛠️ Useful Scripts

Command

Location

Purpose

python manage.py migrate

backend

Apply Django migrations

python manage.py createsuperuser

backend

Create admin login

npm run lint

frontend

Run Angular ESLint

ng build --configuration production

frontend

Prod build

docker compose up -d

root

Spin up MySQL + API + SPA

📑 API Snapshot

Method

Endpoint

Usage

GET

/employees/

List employees

POST

/employees/

Add employee

GET

/trainings/

List trainings

POST

/leave-requests/

Create leave request

PATCH

/leave-requests/:id/approve/

Approve leave

Full OpenAPI spec available at /api/schema/. Use Swagger UI (/api/docs).

📊 Dashboard Preview

Workforce Overview

Training Progress

(screenshots here)

(screenshots here)

Add your own screenshots in docs/screens/ and they will appear above.

🚀 Benefits

Seamless Integration – REST API bridges Angular & Django.

Efficiency Boost – Automated approvals and onboarding workflows.

Employee Empowerment – Self‑service reduces HR overhead.

Data‑Driven Decisions – Real‑time metrics for smarter planning.

🤝 Contributing

Fork → git checkout -b feature/awesome.

Commit → git commit -m 'feat: awesome'.

Push → git push origin feature/awesome.

Open Pull Request.

📄 License

Released under the MIT License. See LICENSE for details.

👨‍💻 Author

Elyes Bassoumi – elyesbassoumi489@gmail.com

Made with ❤️ in Tunisia.Transform your HR workflow today! 💼✨
