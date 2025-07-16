# 📚 Library Management System (C++ & MySQL)

A console-based **Library Management System** built using **C++** and the **MySQL Connector/C** (v6.1.11). This project supports basic administrative and user operations for managing books and student records.

---

## 🚀 Features

### ✅ Admin
- Add new books with quantity.
- Register students into the system.

### 👥 User
- View available books.
- Borrow books if available.
- Validates student identity before issuing.

---

## 💻 Technologies Used

- **C++** — Core application logic.
- **MySQL** — Backend database for storing book and student data.
- **MySQL Connector/C (v6.1.11)** — Connects C++ to MySQL.
- **Windows API (Sleep, system)** — Used for delay and screen clearing (Windows-specific).

---

## 📂 Project Structure
```
Library-Management-UsingMySQL/
│
├── main.cpp # Main application logic
├── README.md # Project description and instructions
├── .gitattributes # Git settings (e.g. line endings)
└── mysql-connector-c-6.1.11-winx64/
├── include/ # MySQL header files (e.g. mysql.h)
└── lib/ # MySQL library files
```
---

## 🛠️ Setup Instructions

### 1. 🔽 Install MySQL Connector/C 6.1.11

Download and extract it from the [MySQL archives](https://downloads.mysql.com/archives/c-c/).

### 2. 🧱 Database Setup

Run the following queries in your MySQL server:

```sql
CREATE DATABASE mydb;

USE mydb;

CREATE TABLE lib (
    Name VARCHAR(255),
    Quantity INT
);

CREATE TABLE student (
    Id VARCHAR(255)
);
```
### 3. 🧾 Update Configuration (Optional)
```
const char* HOST = "localhost";
const char* USER = "root";
const char* PW   = "abc123#";
const char* DB   = "mydb";
```
###4. 🧑‍💻 Compile the Project
```
g++ main.cpp -o LibraryApp.exe ^
  -I"C:\mysql-connector-c-6.1.11-winx64\include" ^
  -L"C:\mysql-connector-c-6.1.11-winx64\lib" ^
  -lmysql
```
###5. ▶️ Run the Application
```
./LibraryApp.exe
