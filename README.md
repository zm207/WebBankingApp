# WebBankingApp

A secure and user-friendly web application built with Django, developed as part of a university project. The application provides core banking functionalities for users to send, receive, and manage financial transactions securely. It also includes an admin interface for monitoring transaction activities and adheres to best practices for secure and efficient web development.

## Features

### User Features
- **Registration and Login**: Secure user authentication system.
- **View Transactions**: Access a history of all incoming and outgoing transactions.
- **Send Money**: Transfer money to other registered users via a dropdown menu.
- **Request Money**: Request payments from other users with a description.
- **Account Security**:
  - CSRF protection.
  - Passwords hashed and securely stored in the database.

### Admin Features
- **View Transactions**: Monitor all user transactions, including accepted and pending payment requests.
- **Admin Authentication**: Admins are labeled as "Superusers" and can access additional monitoring features.

## Architecture and Design
- **Business Logic Layer**: Separates presentation and data access layers.
- **Data Access Layer**: Built with Django's ORM and SQLite database for data storage and integrity.
- **Security Layer**:
  - Protection against CSRF, SQL Injection, and XSS (partially implemented).
  - Access control to restrict unauthorized users.

## Technologies Used
- **Backend**: Django framework
- **Database**: SQLite
- **Frontend**: HTML, CSS
- **Development Environment**: IntelliJ IDEA

## How to Run the Project

### Setup and Run the Server:
1. Clone the repository.
2. Navigate to the project directory.
3. Install dependencies: `pip install -r requirements.txt`.
4. Run the development server: `python manage.py runserver`.
5. Access the app via `http://127.0.0.1:8000/`.

### User Registration:
1. Navigate to the registration page via the homepage.
2. Enter username, email, and password.
3. Select a currency and register.

### Login:
1. Use the registered credentials to log in.
2. Navigate through the platform using the navigation bar.

### Features:
- **Send Money**: Navigate to the "Send Money" page, select a recipient, and specify the amount.
- **Request Money**: Use the "Request Money" page to send payment requests.
- **View Transactions**: Access transaction history through the "Transactions" page.
- **Logout**: Securely log out via the navigation bar.

### Admin Access:
1. Login as admin with:
   - **Username**: `admin1`
   - **Password**: `admin1`
2. View all ongoing transactions and requests.

## Security Considerations
- The project implements CSRF protection and hashed passwords for security.
- HTTPS was not implemented during the development phase but is recommended for deployment.

## Known Limitations
- Partial XSS protection.
- Lack of HTTPS for secure communication.
- The admin cannot intervene in transactions, only monitor them.
