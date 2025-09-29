# Mergington High School Activities

A comprehensive web-based management system that allows students to explore extracurricular activities and enables teachers to manage student registrations at Mergington High School.

## Features

### For Students
- **Browse Activities**: View all available extracurricular activities with detailed descriptions and schedules
- **Advanced Search**: Search activities by name, description, or keywords
- **Smart Filtering**: Filter activities by:
  - Category (Sports, Arts, Academic, Community, Technology)
  - Schedule (Before School, After School, Weekend)
  - Specific days of the week
- **Responsive Design**: Optimized experience across desktop and mobile devices

### For Teachers
- **Secure Authentication**: Login system with password hashing for teacher accounts
- **Student Registration**: Register students for activities on their behalf
- **Student Management**: Remove students from activities when needed
- **Session Management**: Persistent login sessions with validation

### Technical Features
- **RESTful API**: FastAPI-based backend with automatic API documentation
- **Database Integration**: MongoDB for persistent data storage
- **Real-time Updates**: Dynamic content loading without page refreshes
- **Activity Analytics**: Track participant counts and availability
- **Schedule Management**: Detailed time and day scheduling system

## Technology Stack

- **Backend**: FastAPI (Python web framework)
- **Database**: MongoDB with PyMongo driver  
- **Frontend**: Vanilla JavaScript, HTML5, CSS3
- **Authentication**: Argon2 password hashing
- **Server**: Uvicorn ASGI server
- **Styling**: Responsive CSS with mobile-first design

## API Endpoints

The application provides a comprehensive REST API:

- `GET /activities` - List all activities with optional filtering
- `GET /activities/days` - Get available days for activities
- `POST /activities/{activity_name}/signup` - Register student for activity (teacher auth required)
- `POST /activities/{activity_name}/unregister` - Remove student from activity (teacher auth required)
- `POST /auth/login` - Teacher authentication
- `GET /auth/check-session` - Validate teacher session

## Development Guide

For detailed setup and development instructions, please refer to our [Development Guide](../docs/how-to-develop.md).
