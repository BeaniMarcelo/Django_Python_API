# Django Python API

This is a project to test Django with Python.

## Description

A Django REST Framework API project for testing and learning Django functionality. The project includes a simple User model with basic CRUD operations.

## Features

- Django REST Framework integration
- User model with name and age fields
- RESTful API endpoints for user management

## Setup

1. Install dependencies:
```bash
pip install django djangorestframework
```

2. Run migrations:
```bash
python manage.py makemigrations
python manage.py migrate
```

3. Start the development server:
```bash
python manage.py runserver
```

## API Endpoints

- `GET /api/users/` - Retrieve all users
- `POST /api/users/` - Create a new user

