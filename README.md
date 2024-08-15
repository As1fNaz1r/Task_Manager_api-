# Task Management System

This is a task management system built with Flask and PostgreSQL, providing a RESTful API for managing tasks with JWT-based authentication.

## Table of Contents

- [Getting Started](#getting-started)
- [Running the Application Locally](#running-the-application-locally)
- [Approach and Assumptions](#approach-and-assumptions)

## Getting Started

Follow these instructions to set up and run the project on your local machine.

### Prerequisites

- [Docker](https://www.docker.com/get-started)

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
- Framework Choice: Flask was chosen for its simplicity and ease of use in building RESTful APIs.
- Database: PostgreSQL is used as the relational database, and SQLAlchemy is the ORM.
- JWT Authentication: Implemented JWT for securing API endpoints.
Dockerization: Docker is used to ensure consistency across different environments, making the application easily portable.
### Assumptions
- The application assumes well-formed user input and does not include extensive validation or sanitization.
- Tasks are user-specific, meaning each user can only see and manage their own tasks.
