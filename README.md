# Kreshnik Track-Tik Task

## Prerequisites

Before you begin, ensure you have the following installed:

- Docker
- Docker Compose

## Setup

**Build and start the Docker containers:**

    ```sh
    docker-compose up --build
    ```

The application should be running at `http://localhost:8080`.

## Endpoints

### CREATE EMPLOYEE

**URI**
POST http://localhost:8080/employees

**Body examples**
{
  "provider_type": "A",
  "Role": "Store Clerk",
  "Password": "Password123!",
  "Gender": "M",
  "Birthday": "01-01-2000",
  "FullName": "ProviderA ProviderA",
  "Telephone": "555-555-1234",
  "EmailAddress": "aaa@providerA.com"
}

{
  "provider_type": "B",
  "position": "Store Clerk",
  "password": "Password123!",
  "sex": "F",
  "day_of_birth": "10-10-2000",
  "name": "ProviderB",
  "surname": "ProviderB",
  "phone_number": "555-555-4321",
  "email": "bbb@providerB.com"
}

### UPDATE EMPLOYEE

PATCH http://localhost:8080/employees/{id}

**Body examples**

{
  "provider_type": "A",
  "position": "Store Manager",
  "email": "aaa@managment.com"
}

{
  "provider_type": "B",
  "position": "Store Manager",
  "email": "bbb@managment.com"
}
