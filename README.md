#  Bank Application (Java + JDBC)

This project is a **console-based Bank Management System** built using **Java and JDBC**, which allows users to perform banking operations like registration, login, deposit, withdrawal, and balance checking. It also includes an admin module to monitor users and transactions.

---

##  Overview

This application follows a **2-tier architecture**:

- **Client:** Java (Console Application)
- **Server:** MySQL Database

Communication between Java and the database is handled using **JDBC (Type-4 Driver)** :contentReference[oaicite:1]{index=1}.

---

##  Features

###  User Features
- User Registration
- Secure Login (with password hashing)
- Deposit Money
- Withdraw Money
- Check Account Balance

###  Security Features
- Password hashing using **SHA-256** :contentReference[oaicite:2]{index=2}
- No plain-text password storage
- Secure authentication system

###  Admin Features
- View all registered users
- View all transactions :contentReference[oaicite:3]{index=3}

---

##  How It Works

###  Main Flow
The application starts with a menu:
- Register
- Login
- Admin Login
- Exit :contentReference[oaicite:4]{index=4}

After login:
- Users can perform transactions
- Admin can monitor system data

---

##  Database Design

The project uses MySQL with the following tables:

###  Users Table
- user_id
- username
- password (hashed)
- balance

###  Transactions Table
- transaction_id
- user_id
- transaction_type (deposit/withdrawal)
- amount

###  Admin Table
- admin credentials

(SQL file provided: `projectBankApplication.sql`) 

---

##  Database Connection

Connection is handled using JDBC:

```java
DriverManager.getConnection(URL, USER, PASSWORD);

## Project Structure

project_bankApplication/
│
├── BankApplication.java        # Main entry point
├── UserRegistration.java       # User signup logic
├── UserLogin.java              # Login system
├── UserOperations.java         # Balance check
├── TransactionService.java     # Deposit & withdrawal
├── AdminOperations.java        # Admin features
├── PasswordUtils.java          # Password hashing
├── SetConnection.java          # DB connection
├── projectBankApplication.sql  # Database schema
├── Bank Application Project.pdf
