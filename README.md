# Learning Platform Demo

A 3-tier containerized learning platform application.

## Architecture

- **Frontend**: React.js (Port 3000)
- **Backend**: Python FastAPI (Port 8000)
- **Database**: PostgreSQL (Port 5432)

## Features

- View all courses
- Add new courses
- Delete courses
- RESTful API

## Running the Application

```bash
# Build and start all services
docker-compose up --build

# Run in detached mode
docker-compose up -d --build

# Stop all services
docker-compose down

# Stop and remove volumes
docker-compose down -v
```

## Access

- Frontend: http://localhost:3000
- Backend API: http://localhost:8000
- API Docs: http://localhost:8000/docs

## Database Credentials

- Database: learning_platform
- User: admin
- Password: admin123
