# User Management System - Backend

This is the backend for the User Management System, built with Go and PostgreSQL.

## Prerequisites

- Go 1.18 or higher
- PostgreSQL

## Setup

1. Create a PostgreSQL database:

```bash
createdb ums_db
```

2. Initialize the database schema:

```bash
psql -d ums_db -f schema.sql
```

3. Update the database connection string in `cmd/main.go` if needed.

4. Install dependencies:

```bash
go mod download
```

5. Run the server:

```bash
go run cmd/main.go
```

The server will start on port 8080.

## API Endpoints

### Authentication

- `POST /api/register` - Register a new user
- `POST /api/login` - Login a user

### Users

- `GET /api/users` - Get all users
- `GET /api/users/{id}` - Get a specific user
- `PUT /api/users/{id}` - Update a user
- `DELETE /api/users/{id}` - Delete a user

## Request/Response Examples

### Register a User

Request:
```json
POST /api/register
{
  "username": "john_doe",
  "password": "password123",
  "email": "john@example.com"
}
```

Response:
```json
{
  "id": "1",
  "username": "john_doe",
  "email": "john@example.com",
  "is_admin": false,
  "created_at": "2023-04-10T12:00:00Z",
  "updated_at": "2023-04-10T12:00:00Z"
}
```

### Login

Request:
```json
POST /api/login
{
  "username": "john_doe",
  "password": "password123"
}
```

Response:
```json
{
  "id": "1",
  "username": "john_doe",
  "email": "john@example.com",
  "is_admin": false,
  "created_at": "2023-04-10T12:00:00Z",
  "updated_at": "2023-04-10T12:00:00Z"
}
```
