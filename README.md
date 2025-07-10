# 🎓 School Management System – Java MySQL JDBC CRUD Project

This is a **console-based Java application** using **JDBC (Java Database Connectivity)** to perform CRUD (Create, Read, Update, Delete) operations on a `teacher` table in a MySQL database.

---

## 💡 Features

- 📥 Add a new teacher
- 📝 Update teacher details (currently updates name only)
- ❌ Delete a teacher by ID
- 🧹 Delete all teacher records
- 🔍 View a teacher by ID
- 📄 View all teacher records
- 🚪 Exit the application

---

## 🛠️ Technologies Used

- Java (JDK 8 or higher)
- JDBC API
- MySQL (v5.7+ or 8.0+)
- MySQL Connector/J Driver

---

## 🧑‍🏫 Database Table Structure

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
🚀 How to Run
1. 📦 Prerequisites
Java Development Kit (JDK) installed

MySQL Server running

MySQL Connector/J JAR file downloaded

2. 🔧 Configuration
Update your database connection string in TeacherJDBC.java:

java
Copy
Edit
Connection connection = DriverManager.getConnection(
    "jdbc:mysql://localhost:3306/Teachers?user=root&password=root");
🔁 Replace root and password with your actual MySQL credentials.

3. ▶️ Compile and Run
On Linux/macOS:

bash
Copy
Edit
javac -cp .:mysql-connector-java-<version>.jar com/jdbc/JDBCExample/TeacherJDBC.java
java -cp .:mysql-connector-java-<version>.jar com.jdbc.JDBCExample.TeacherJDBC
On Windows:

bash
Copy
Edit
javac -cp .;mysql-connector-java-<version>.jar com\jdbc\JDBCExample\TeacherJDBC.java
java -cp .;mysql-connector-java-<version>.jar com.jdbc.JDBCExample.TeacherJDBC
Replace <version> with the actual version number of the MySQL Connector JAR you downloaded.

📋 Sample Menu (Console Output)
markdown
Copy
Edit
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
Uses PreparedStatement to avoid SQL injection.

Input validation and error handling can be improved for production-grade apps.

Ensure the MySQL JDBC driver is in your classpath when running the app.

📬 Future Improvements
Allow updating all teacher fields, not just the name.

Add modularity to code (e.g., split UI and DB logic).

Integrate logging (e.g., using java.util.logging or Log4j).

Create a GUI version using Java Swing or JavaFX.

