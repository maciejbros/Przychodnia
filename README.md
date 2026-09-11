# Przychodnia

A full-stack web application for managing a medical clinic. The system provides functionality for managing patients, appointments, medical data, and clinic users.

The project consists of an Angular frontend and an ASP.NET Core Web API backend with a layered architecture.

## Overview

The application was developed as a practical project to implement a complete clinic management system with a separate frontend and backend.

The system is designed to support different types of users and provide dedicated functionality depending on their role.

### Main areas of the system

* Patient management
* Appointment management
* User authentication and authorization
* Role-based access
* Medical data management
* Prescription and referral management
* Administrative functionality
* PDF document generation
* QR code generation
* REST API communication

## Features

### Authentication and Authorization

* User authentication using JWT
* Role-based access control
* Protected API endpoints
* Separate permissions depending on the user's role

### Patient Management

* Creating and managing patient records
* Viewing patient information
* Access to patient-related medical data

### Appointment Management

* Managing clinic appointments
* Scheduling and modifying appointments
* Managing appointment-related information

### Medical Documentation

* Managing medical records
* Creating medical notes
* Managing prescriptions
* Managing referrals
* Generating PDF documents

### Administration

* User management
* Managing system data
* Administrative access to application functionality

### Additional Features

* REST API
* Swagger API documentation
* QR code generation
* PDF generation
* Automated tests
* Layered backend architecture

## Architecture

The backend follows a layered architecture that separates responsibilities between individual projects.

```text
Przychodnia
│
├── Przychodnia-Angular
│   ├── public
│   └── src
│
└── Przychodnia-WebApi
    ├── Przychodnia.API
    ├── BLL
    ├── DAL
    ├── DTOs
    ├── IBLL
    ├── IDAL_
    ├── Models
    ├── Przychodnia
    ├── BLLTests
    ├── Przychodnia.Tests
    └── Przychodnia.API.Tests
```

### Backend Layers

| Layer             | Responsibility                                                      |
| ----------------- | ------------------------------------------------------------------- |
| `Przychodnia.API` | REST API, controllers, authentication and application configuration |
| `BLL`             | Business logic and application services                             |
| `IBLL`            | Interfaces for business logic services                              |
| `DAL`             | Data access and database communication                              |
| `IDAL_`           | Interfaces for data access                                          |
| `DTOs`            | Data transfer objects used by the API                               |
| `Models`          | Domain and database models                                          |

This separation allows the application logic, data access and API layer to remain independent and easier to maintain.

## Technologies

### Backend

* C#
* .NET 8
* ASP.NET Core Web API
* Entity Framework Core
* SQL
* JWT Authentication
* REST API
* Swagger / OpenAPI
* PDFSharpCore
* QRCoder
* System.IdentityModel.Tokens.Jwt

### Frontend

* Angular 19
* TypeScript
* HTML
* CSS
* RxJS
* Angular Router
* Angular Forms

### Testing

* xUnit
* ASP.NET Core integration testing
* Unit testing of business logic

## API

The backend exposes a REST API used by the Angular frontend.

Swagger/OpenAPI is included to simplify API development and testing.

The API is responsible for:

* Authentication
* Authorization
* Patient operations
* Appointment operations
* Medical data
* User management
* Document generation
* Communication with the database

## Testing

The backend contains separate test projects for different application layers:

```text
BLLTests
Przychodnia.Tests
Przychodnia.API.Tests
```

Tests cover business logic and API functionality.

## Getting Started

### Prerequisites

Make sure the following tools are installed:

* .NET 8 SDK
* Node.js
* npm
* SQL Server
* Angular CLI

### Clone the repository

```bash
git clone https://github.com/maciejbros/Przychodnia.git
cd Przychodnia
```

### Backend

Navigate to the Web API directory:

```bash
cd Przychodnia-WebApi
```

Restore dependencies:

```bash
dotnet restore
```

Build the solution:

```bash
dotnet build
```

Run the API:

```bash
dotnet run --project Przychodnia.API
```

The API will start using the configuration defined in the project.

### Frontend

Open another terminal and navigate to:

```bash
cd Przychodnia-Angular
```

Install dependencies:

```bash
npm install
```

Start the Angular development server:

```bash
npm start
```

The application will be available at:

```text
http://localhost:4200
```

## Project Structure

### Frontend

```text
Przychodnia-Angular/
├── public/
├── src/
├── angular.json
├── package.json
├── package-lock.json
├── tsconfig.json
└── tsconfig.app.json
```

### Backend

```text
Przychodnia-WebApi/
├── BLL/
├── BLLTests/
├── DAL/
├── DTOs/
├── IBLL/
├── IDAL_/
├── Models/
├── Przychodnia/
├── Przychodnia.API/
├── Przychodnia.API.Tests/
├── Przychodnia.Tests/
└── Przychodnia.sln
```

## Development Practices

The project demonstrates several practices commonly used in modern .NET applications:

* Layered architecture
* Separation of concerns
* Dependency injection
* Interface-based programming
* DTOs for API communication
* JWT-based authentication
* RESTful API design
* Unit and integration testing
* Separation of frontend and backend applications

## Purpose of the Project

The project was created as a practical full-stack application to gain experience in designing and developing a larger web system.

It demonstrates experience with:

* C# and .NET
* ASP.NET Core Web API
* Angular and TypeScript
* SQL and Entity Framework Core
* REST APIs
* Authentication and authorization
* Layered architecture
* Automated testing
* Git and GitHub

## Author

**Maciej**

GitHub: https://github.com/maciejbros
