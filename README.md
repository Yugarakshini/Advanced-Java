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

##  How to Run
# 1.  Prerequisites
JDK installed

MySQL Server running

MySQL Connector JAR (Download from MySQL Connector/J)

# 2. 🔧 Configuration
Update your database connection string in TeacherJDBC.java:

java
Copy
Edit
Connection connection = DriverManager.getConnection(
    "jdbc:mysql://localhost:3306/Teachers?user=root&password=root");
Replace root and password with your MySQL credentials.

# 3. ▶️ Compile and Run
bash
Copy
Edit
javac -cp .:mysql-connector-java-<version>.jar com/jdbc/JDBCExample/TeacherJDBC.java
java -cp .:mysql-connector-java-<version>.jar com.jdbc.JDBCExample.TeacherJDBC
On Windows, replace : with ; in classpath.

Sample Menu (Console Output)

===== MENU =====
1. ADD new Teacher
2. UPDATE Existing Teacher details
3. DELETE Teacher details
4. DELETE ALL Teacher's details
5. View Teacher details
6. VIEW ALL Teachers Details
7. Exit
Enter your choice:
📌 Notes
Uses PreparedStatement for SQL injection safety.

Input validation and exception handling should be enhanced for production use.

Make sure MySQL JDBC Driver is in your classpath.

📬 Future Improvements
Update all teacher fields (not just name)

Modularize UI

Add logging

Add GUI using Swing or JavaFX





Here is a sample `README.md` file for your JDBC-based Java project that manages teacher records:

---

````markdown
# TeacherJDBC – Java MySQL JDBC CRUD Project

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

Database: `Teachers`  
Table: `teacher`

```sql
CREATE DATABASE IF NOT EXISTS Teachers;

USE Teachers;

CREATE TABLE IF NOT EXISTS teacher (
    id INT PRIMARY KEY,
    teachername VARCHAR(100) NOT NULL,
    age INT,
    dept VARCHAR(100),
    dob DATE,
    salary DOUBLE
);
````

---

## 🚀 How to Run

### 1. 📦 Prerequisites

* JDK installed
* MySQL Server running
* MySQL Connector JAR (Download from [MySQL Connector/J](https://dev.mysql.com/downloads/connector/j/))

### 2. 🔧 Configuration

Update your database connection string in `TeacherJDBC.java`:

```java
Connection connection = DriverManager.getConnection(
    "jdbc:mysql://localhost:3306/Teachers?user=root&password=root");
```

Replace `root` and `password` with your MySQL credentials.

### 3. ▶️ Compile and Run

```bash
javac -cp .:mysql-connector-java-<version>.jar com/jdbc/JDBCExample/TeacherJDBC.java
java -cp .:mysql-connector-java-<version>.jar com.jdbc.JDBCExample.TeacherJDBC
```

On Windows, replace `:` with `;` in classpath.

---

## 📷 Sample Menu (Console Output)

```
===== MENU =====
1. ADD new Teacher
2. UPDATE Existing Teacher details
3. DELETE Teacher details
4. DELETE ALL Teacher's details
5. View Teacher details
6. VIEW ALL Teachers Details
7. Exit
Enter your choice:
```

---

## 📌 Notes

* Uses `PreparedStatement` for SQL injection safety.
* Input validation and exception handling should be enhanced for production use.
* Make sure MySQL JDBC Driver is in your classpath.

---

## 📬 Future Improvements

* Update all teacher fields (not just name)
* Modularize UI
* Add logging
* Add GUI using Swing or JavaFX





