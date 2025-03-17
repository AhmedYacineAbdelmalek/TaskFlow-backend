# TaskFlow Backend

TaskFlow is a mobile task management app developed as a final year project (PFE). This repository contains the FastAPI backend for TaskFlow, providing secure user authentication, task management, and more.

## Features

- **User Authentication:** Secure signup and login endpoints using JWT.
- **Task Management:** CRUD operations for creating, reading, updating, and deleting tasks.
- **Scheduled Tasks:** Automated scheduling of recurring tasks.
- **Push Notifications:** Endpoints to trigger reminders and notifications.
- **Database Integration:** PostgreSQL with SQLAlchemy ORM and Alembic migrations.

## Tech Stack

- **[FastAPI](https://fastapi.tiangolo.com/):** High-performance web framework for Python.
- **[PostgreSQL](https://www.postgresql.org/):** Robust relational database.
- **[SQLAlchemy](https://www.sqlalchemy.org/):** ORM for database interactions.
- **[Alembic](https://alembic.sqlalchemy.org/):** Database migrations.
- **[Python-Jose](https://github.com/mpdavis/python-jose):** JWT token management.
- **[Passlib](https://passlib.readthedocs.io/):** Secure password hashing.
- **[Pydantic](https://pydantic-docs.helpmanual.io/):** Data validation and settings management.

## Project Structure
TaskFlow-backend/
├── alembic/                
│   └── ...                # Database migration scripts managed by Alembic
├── alembic.ini            # Global configuration for Alembic migrations
├── app/                   
│   ├── __init__.py        # Marks this directory as a Python package
│   ├── main.py            # FastAPI application entry point
│   ├── config.py          # Application configuration (e.g., loading .env settings)
│   ├── database.py        # Database connection setup and session management using SQLAlchemy
│   ├── models.py          # SQLAlchemy models (e.g., the User model)
│   ├── auth.py            # Authentication utilities (JWT handling, password hashing, etc.)
│   └── routes/            
│         ├── __init__.py  # Initializes the routes package
│         └── user_routes.py  # User authentication endpoints (signup, login)
├── .env                   # Environment variable definitions (sensitive configuration)
├── requirements.txt       # List of Python dependencies for the project
└── .gitignore             # Specifies files and directories for Git to ignore

