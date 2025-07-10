# School Management System – Java MySQL JDBC CRUD Project

This is a **console-based Java application** using **JDBC (Java Database Connectivity)** to perform CRUD (Create, Read, Update, Delete) operations on a `teacher` table in a MySQL database.

---

## 💡 Features

- 📥 **Add** a new teacher
- 📝 **Update** teacher details (currently updates name only)
- ❌ **Delete** a teacher by ID
- 🧹 **Delete all** teacher records
- 🔍 **View** a teacher by ID
- 📄 **View all** teacher records
- 📤 Exit the application safely

---

## 🛠️ Technologies Used

- Java (JDK 8 or higher)
- JDBC API
- MySQL (v5.7+ or 8.0+)
- MySQL Connector/J Driver

---

## 🧑‍🏫 Table Structure

Database: `school`  
Table: `teacher`

```sql

USE school;

CREATE TABLE IF NOT EXISTS teacher (
    id INT PRIMARY KEY,
    teachername VARCHAR(100) NOT NULL,
    age INT,
    dept VARCHAR(100),
    dob DATE,
    salary DOUBLE
);
