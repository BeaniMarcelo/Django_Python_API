<img width="839" height="211" alt="image" src="https://github.com/user-attachments/assets/7ec2686a-71ba-4446-ac6f-7666ac737e84" /># Django Python API

This is a project to test Django with Python.

## Description

A Django REST Framework API project for testing and learning Django functionality. The project includes a simple User model with basic CRUD operations.

<img width="907" height="816" alt="image" src="https://github.com/user-attachments/assets/3fe15de8-8489-451f-9395-f1c0084c21db" />
<img width="916" height="883" alt="image" src="https://github.com/user-attachments/assets/5b0b3bdb-7245-424a-8d86-12eb5c95279a" />
<img width="839" height="211" alt="image" src="https://github.com/user-attachments/assets/ff48c827-e39e-4698-9804-b31b6712e0ef" />



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

