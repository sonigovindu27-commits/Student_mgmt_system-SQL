
# 🎓 Student Management System – SQL Project

## 📌 Project Overview
The Student Management System is a SQL-based project designed to store, manage, and analyze student information efficiently.  
It demonstrates the use of SQL for database creation, data manipulation, and analytical queries on student academic records.

---

## 🧑‍💻 Author
**Soni Govindu**

---

## 🛠 Tools & Technologies
- SQL  
- MySQL  
- XAMPP / MySQL Workbench  

---

## 🗂 Database Information
- **Database Name:** `stu_mgmt`
- **Table Name:** `students`

---

## 📋 Table Structure

### students

| Column Name | Data Type | Description |
|------------|----------|-------------|
| student_id | INT (Primary Key) | Unique student identifier |
| first_name | VARCHAR(50) | Student first name |
| last_name | VARCHAR(50) | Student last name |
| gender | VARCHAR(10) | Gender |
| dob | DATE | Date of birth |
| course | VARCHAR(50) | Course enrolled |
| email | VARCHAR(100) | Unique email ID |
| phone | VARCHAR(15) | Contact number |
| admission_date | DATE | Date of admission |
| marks | DECIMAL(5,2) | Student marks |

---

## ✨ Features Implemented

### Database Operations
- Create and use database
- Create table with constraints
- Insert student records

### CRUD Operations
- View all students
- Update student marks
- Delete student records

### SQL Analysis
- Calculate average marks
- Find highest and lowest marks
- Course-wise student count
- Identify students scoring above average

### Advanced SQL Concepts
- Aggregate functions
- GROUP BY
- Subqueries
- ORDER BY
- Views

---

## 📊 Sample Queries

### View All Students
```sql
SELECT * FROM students;
