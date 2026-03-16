# User Management API

Backend application for managing users.  
The system provides basic CRUD operations (Create, Read, Update, Delete) for user entities and demonstrates a typical layered backend architecture using Spring Boot.

## Technologies

- Java
- Spring Boot
- Spring Data JPA
- PostgreSQL
- Maven

## Features

- Create a new user
- Retrieve all users
- Update an existing user
- Delete a user

## Project Structure

```
com.example.usermanagement
│
├── controller
│   └── UserController
│
├── service
│   └── UserService
│
├── repository
│   └── UserRepository
│
├── entity
│   └── User
│
└── UserManagementApplication
```

## API Endpoints

| Method | Endpoint | Description |
|------|------|------|
| GET | /users | Get all users |
| POST | /users | Create a new user |
| PUT | /users/{id} | Update user |
| DELETE | /users/{id} | Delete user |

## Example Request

Create user:

POST /users

```json
{
  "name": "Dana",
  "age": 30
}
```

## Running the Application

1. Clone the repository
2. Configure the PostgreSQL connection in `application.properties`
3. Run the Spring Boot application

The server will start at:

```
http://localhost:8080
```

## Purpose

This project was created as a learning exercise to demonstrate building a simple REST API using Spring Boot and connecting it to a relational database.
