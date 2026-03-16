# User Management API

Backend service for managing users and user-related operations.  
The system exposes RESTful endpoints for creating, retrieving, updating, and deleting users, and follows a layered architecture commonly used in modern backend applications.

The application is built using Spring Boot and connects to a PostgreSQL database using Spring Data JPA.

## Technologies

- Java
- Spring Boot
- Spring Data JPA
- PostgreSQL
- Maven
- REST API

## Features

- Create new users
- Retrieve all users
- Retrieve user by ID
- Update existing users
- Delete users
- Input validation
- Exception handling
- Pagination and sorting for user lists
- Database persistence using JPA
- Layered architecture (Controller / Service / Repository)
- JSON-based API communication

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
├── exception
│   └── GlobalExceptionHandler
│
└── UserManagementApplication
```

## API Endpoints

| Method | Endpoint | Description |
|------|------|------|
| GET | /users | Retrieve all users |
| GET | /users/{id} | Retrieve a user by ID |
| POST | /users | Create a new user |
| PUT | /users/{id} | Update an existing user |
| DELETE | /users/{id} | Delete a user |

## Example Request

Create user:

POST /users

```json
{
  "name": "Dan",
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

## Database

The application uses PostgreSQL as the relational database and maps entities using Spring Data JPA.

Example table:

```
users
-----
id
first_name
last_name
email
age
phone_number
role
status
created_at
updated_at
```

### Field Description

| Field | Description |
|------|------|
| id | Unique identifier of the user |
| first_name | User's first name |
| last_name | User's last name |
| email | User email address |
| age | User age |
| phone_number | Contact phone number |
| role | User role (e.g., ADMIN, USER) |
| status | Account status (ACTIVE, INACTIVE) |
| created_at | Timestamp when the user was created |
| updated_at | Timestamp of the last update |
