# Django Python API - Full Stack Application

A full-stack web application built with Django REST Framework (backend) and Vue.js 3 (frontend) for user management.

## 📋 Table of Contents

- [Description](#description)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Project Structure](#project-structure)
- [Prerequisites](#prerequisites)
- [Installation & Setup](#installation--setup)
- [Running the Application](#running-the-application)
- [API Endpoints](#api-endpoints)
- [Frontend Features](#frontend-features)
- [Development](#development)
- [Repositories](#repositories)

## 📝 Description

This project is a full-stack web application designed to test and demonstrate Django with Python. It consists of:

- **Backend**: Django REST Framework API that provides RESTful endpoints for user management
- **Frontend**: Modern Vue.js 3 application with a responsive UI for interacting with the API

The application allows users to create and view user records through an intuitive web interface, demonstrating the integration between a Python backend and a JavaScript frontend.

## ✨ Features

### Backend Features
- Django REST Framework integration
- User model with name and age fields
- RESTful API endpoints for user management
- CORS configuration for frontend communication
- SQLite database for data storage

### Frontend Features
- **User Management**: Create and view users through a web interface
- **Modern UI**: Clean, responsive design with gradient backgrounds
- **Real-time Updates**: Automatically refreshes user list after creating a new user
- **Error Handling**: Displays user-friendly error messages
- **Loading States**: Visual feedback during API requests

## 🛠 Tech Stack

### Backend
- **Python 3**
- **Django 6.0** - Web framework
- **Django REST Framework** - API framework
- **django-cors-headers** - CORS handling
- **SQLite** - Database

### Frontend
- **Vue.js 3** - Progressive JavaScript framework
- **Vite** - Build tool and dev server
- **Axios** - HTTP client for API requests
- **JavaScript (ES6+)** - Programming language

## 📁 Project Structure

```
Django_Python_API/
├── api/                          # Django app
│   ├── models.py                # User model definition
│   ├── views.py                 # API views (GET, POST)
│   ├── serializer.py            # DRF serializers
│   ├── urls.py                  # API routes
│   └── migrations/              # Database migrations
├── Django_Python_API/            # Django project settings
│   ├── settings.py              # Project configuration (CORS, apps, etc.)
│   ├── urls.py                  # Main URL configuration
│   └── wsgi.py                  # WSGI configuration
├── frontend/                     # Vue.js frontend (separate repository)
│   ├── src/
│   │   ├── App.vue              # Main Vue component
│   │   ├── main.js              # Vue app initialization
│   │   ├── style.css            # Global styles
│   │   └── services/
│   │       └── api.js           # API service
│   ├── index.html               # HTML entry point
│   ├── package.json             # Frontend dependencies
│   └── vite.config.js           # Vite configuration
├── manage.py                     # Django management script
├── db.sqlite3                    # SQLite database (generated)
└── README.md                     # This file
```

## 📦 Prerequisites

Before you begin, ensure you have the following installed:

- **Python 3.8+** - [Download Python](https://www.python.org/downloads/)
- **Node.js 16+** and **npm** - [Download Node.js](https://nodejs.org/)
- **Git** - [Download Git](https://git-scm.com/downloads)

## 🚀 Installation & Setup

### Backend Setup

1. **Clone the repository** (if you haven't already):
```bash
git clone https://github.com/BeaniMarcelo/Django_Python_API.git
cd Django_Python_API
```

2. **Install Python dependencies**:
```bash
pip install django djangorestframework django-cors-headers
```

3. **Run database migrations**:
```bash
python manage.py makemigrations
python manage.py migrate
```

### Frontend Setup

1. **Navigate to the frontend directory**:
```bash
cd frontend
```

2. **Install Node.js dependencies**:
```bash
npm install
```

> **Note**: The frontend is in a separate repository. If you need to clone it separately:
> ```bash
> git clone https://github.com/BeaniMarcelo/Django_Python_API_Frontend.git
> cd Django_Python_API_Frontend
> npm install
> ```

## 🏃 Running the Application

### Start the Backend Server

1. **Navigate to the Django project root**:
```bash
cd Django_Python_API
```

2. **Start the Django development server**:
```bash
python manage.py runserver
```

The backend API will be available at: `http://localhost:8000`

### Start the Frontend Server

1. **Navigate to the frontend directory**:
```bash
cd frontend
```

2. **Start the Vue.js development server**:
```bash
npm run dev
```

The frontend will be available at: `http://localhost:5173`

### Access the Application

Open your browser and navigate to: **http://localhost:5173**

You should see the User Management System interface where you can:
- View all existing users
- Create new users by filling in the form

## 🔌 API Endpoints

The Django backend provides the following REST API endpoints:

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET` | `/api/users/` | Retrieve all users |
| `POST` | `/api/users/create` | Create a new user |

### Example API Requests

**Get all users:**
```bash
curl http://localhost:8000/api/users/
```

**Create a user:**
```bash
curl -X POST http://localhost:8000/api/users/create \
  -H "Content-Type: application/json" \
  -d '{"name": "John Doe", "age": 30}'
```

### Example Response

```json
[
  {
    "id": 1,
    "name": "John Doe",
    "age": 30
  },
  {
    "id": 2,
    "name": "Jane Smith",
    "age": 25
  }
]
```

## 🎨 Frontend Features

The Vue.js frontend provides:

- **User List Display**: Grid layout showing all users with their details
- **Create User Form**: Simple form with name and age fields
- **Success/Error Messages**: Visual feedback for user actions
- **Loading States**: Indicators during API requests
- **Responsive Design**: Works on desktop and mobile devices

## 💻 Development

### Backend Development

- The Django backend uses SQLite by default (configured in `settings.py`)
- API views are defined in `api/views.py`
- Serializers are in `api/serializer.py`
- URL routing is configured in `api/urls.py`

### Frontend Development

- The frontend uses Vite for fast development and hot module replacement
- API service is configured in `src/services/api.js`
- Main component logic is in `src/App.vue`
- Vite proxy is configured to forward `/api` requests to `http://localhost:8000`

### CORS Configuration

CORS is configured in Django settings to allow requests from:
- `http://localhost:5173` (Vite dev server)
- `http://localhost:3000` (alternative port)
- `http://127.0.0.1:5173` and `http://127.0.0.1:3000`

## 📚 Repositories

This project consists of two separate repositories:

- **Backend**: [Django_Python_API](https://github.com/BeaniMarcelo/Django_Python_API)
- **Frontend**: [Django_Python_API_Frontend](https://github.com/BeaniMarcelo/Django_Python_API_Frontend)

## 📄 License

This project is for educational and testing purposes.

## 👤 Author

Marcelo Beani

---

**Note**: This is a project to test Django with Python and demonstrate full-stack development with Django REST Framework and Vue.js.
