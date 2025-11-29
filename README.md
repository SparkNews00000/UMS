# UMS Project

## Overview
The UMS (User Management System) project is a web application that allows users to sign up, sign in, and manage their profiles (admin). Admin users have additional privileges to manage all users within the system. The application is built using React for the frontend and Go for the backend, with PostgreSQL as the database.

## Technologies Used
- **Frontend**: React, TypeScript, Vite, Material UI, Axios
- **Backend**: Go, PostgreSQL

## Features
1. User registration and login functionality.
2. User data is stored in a PostgreSQL database.
3. A simple homepage for users after logging in.
4. Admin panel for managing users.
5. A left sidebar for easy navigation between pages.
6. Axios for making RESTful API calls to the backend.

## Setup Instructions

### Frontend
1. Navigate to the `frontend` directory.
2. Install dependencies:
   ```
   npm install
   ```
3. Start the development server:
   ```
   npm run dev
   ```

### Backend
1. Navigate to the `backend` directory.
2. Install dependencies:
   ```
   go mod tidy
   ```
3. Run the backend server:
   ```
   go run cmd/main.go
   ```

### Database
1. Set up a PostgreSQL database and configure the connection in `backend/internal/db/connection.go`.
2. Run the SQL migration scripts located in `db/migrations` to create the necessary tables.


## Usage
- Access the application through the frontend URL (usually `http://localhost:3000`).
- Use the login and registration pages to create and manage user accounts.
- Admin users can access the admin panel to manage all users.


## Contributing
Contributions are welcome! Please submit a pull request or open an issue for any enhancements or bug fixes.

