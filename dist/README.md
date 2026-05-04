# BookShop1 — Library Management System

A desktop Library Management System built with **Java Swing** and **MySQL**, developed in NetBeans IDE.

## Features

### Login & Access Control
- Role-based login (Admin / User) with username, password, and role selection
- Splash screen with animated progress bar on startup

### Books Management
- Add, edit, delete books
- Fields: Book ID, Name, Author, Category, Price, Quantity
- View all books in a searchable table
- Print book records

### Billing
- Generate bills by selecting books from inventory
- Auto-calculates total and grand total
- Supports multiple items per bill
- Print bill functionality with client name and bill number

### User Management
- Add and manage users (User ID, Name, Password, Phone, Address)
- View all users in a table

## Tech Stack

| Layer | Technology |
|-------|------------|
| Language | Java |
| UI Framework | Java Swing (JFrame, JTable, JComboBox) |
| Database | MySQL via JDBC |
| IDE | NetBeans |
| Build | Apache Ant |

## Project Structure

```
BookShop1/
├── src/
│   └── bookshop1/
│       ├── BookShop1.java   — Entry point (main class)
│       ├── Splash.java      — Splash screen with progress bar
│       ├── Login.java       — Role-based login with SQL auth
│       ├── Books.java       — Book inventory management
│       ├── Biling.java      — Billing and receipt generation
│       └── Users.java       — User account management
├── dist/
│   └── BookShop1.jar        — Executable JAR
└── README.md
```

## How to Run

### Option 1 — Run the JAR directly
```bash
java -jar dist/BookShop1.jar
```
Or double-click `BookShop1.jar` in File Explorer.

### Option 2 — Open in NetBeans
1. File → Open Project
2. Navigate to this folder
3. Click Open Project
4. Set up MySQL connection in the source files
5. Run → Run Project

## Database Setup

The app connects to a MySQL database. Before running from source, create the database:

```sql
CREATE DATABASE bookshop;
USE bookshop;

CREATE TABLE books (
    book_id VARCHAR(20) PRIMARY KEY,
    name VARCHAR(100),
    author VARCHAR(100),
    category VARCHAR(50),
    price DOUBLE,
    quantity INT
);

CREATE TABLE users (
    uid VARCHAR(20) PRIMARY KEY,
    uname VARCHAR(100),
    password VARCHAR(100),
    phone VARCHAR(15),
    address VARCHAR(200)
);

CREATE TABLE billing (
    bill_no VARCHAR(20),
    client_name VARCHAR(100),
    book_name VARCHAR(100),
    qty INT,
    price DOUBLE,
    total DOUBLE
);
```

## Screenshots

> UI built with Java Swing featuring panels, tables, and form inputs for each module.

## Author

**Aryan Grang** — B.Sc. Computer Science, Krea University
