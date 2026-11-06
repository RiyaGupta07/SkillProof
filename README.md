# SkillProof – Skill Verification Platform

SkillProof is a backend application designed to provide a platform for managing and verifying users' skills and competencies.

**Project Status:** Work in Progress 🚧

## Tech Stack
- Java
- Spring Boot
- Spring Security
- Spring Data JPA
- MySQL
- Maven
- Postman

## Implemented Features
- User registration REST API
- Server-side email validation
- Duplicate account checking
- BCrypt password encryption
- Automatic default role assignment
- Database persistence

## Architecture

SkillProof follows a layered Spring Boot architecture.

### Registration Flow

1. The client sends a registration request to `POST /api/auth/register`.
2. `AuthController` receives the request through `RegisterRequest`.
3. `AuthService` validates the registration details and checks for duplicate email addresses.
4. Passwords are securely hashed using BCrypt.
5. New users are assigned the default `STUDENT` role and `LOCAL` authentication provider.
6. `UserRepository` persists the user entity in MySQL.
7. The API returns a `UserResponse` without exposing sensitive password information.


### Current Implementation

- User registration REST API
- Email validation and duplicate-account checks
- BCrypt password hashing
- Default role and authentication provider assignment
- MySQL persistence using Spring Data JPA

**Note:** Login, JWT authentication and role-based authorization are planned features and are not yet implemented.
## Upcoming Features
- User login and authentication
- JWT-based authentication
- Role-based authorization
- Skill management and verification
- Protected REST API endpoints
- Unit and integration testing

## Getting Started

1. Clone this repository.
2. Open the project in IntelliJ IDEA.
3. Configure your MySQL database credentials.
4. Build the project using Maven.
5. Run the Spring Boot application.

## Project Status

This project is actively under development. Additional authentication, authorization, and skill verification features will be implemented in upcoming iterations.
