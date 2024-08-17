# Task Management System

This is a task management system built with Flask and PostgreSQL, providing a RESTful API for managing tasks with JWT-based authentication.

## Table of Contents

- [Getting Started](#getting-started)
- [Features](#features)
- [Technologies](#technologies)
- [Running the Application Locally](#running-the-application-locally)
- [Approach and Assumptions](#approach-and-assumptions)

## Getting Started

Follow these instructions to set up and run the project on your local machine.

### Prerequisites

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/)
- [Git](https://git-scm.com/)

  
### Clone the Repository

git clone https://github.com/As1fNaz1r/Task_Manager_api-
cd task_manager_api

  ## Features

- User registration and authentication with JWT.
- CRUD operations for tasks.
- Role-based access control for task management.
- Dockerized setup for easy deployment.

## Technologies

- **Backend:** Flask, Flask-SQLAlchemy
- **Database:** PostgreSQL
- **Authentication:** Flask-JWT-Extended
- **Containerization:** Docker, Docker Compose
- **Documentation:** Postman

## Running the Application Locally
#### Set Up Environment Variables
Create a .env file in the root directory with the following content:
- SECRET_KEY=your_secret_key
- JWT_SECRET_KEY=your_jwt_secret_key
- DATABASE_URL=postgresql://postgres:postgres@localhost:5432/tasksDB


#### Build and Run the Application with Docker
Ensure Docker is installed and running on your machine. Then, execute:
- docker-compose up --build

#### Access the Application
The API will be available at http://localhost:5000.

#### Database Migrations
If you make changes to the models and need to apply them, run:
- docker-compose exec web flask db migrate
- docker-compose exec web flask db upgrade

## Approach and Assumptions
#### Approach

- The application follows a RESTful API design.
- Docker is used for containerization, making the application easy to deploy on different environments.
- Flask-SQLAlchemy is used to interact with the PostgreSQL database.

### Assumptions
- The application is designed as a proof-of-concept for task management.
- The focus was on setting up a functional API with basic authentication and task management features.
