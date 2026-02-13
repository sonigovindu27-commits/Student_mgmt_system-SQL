-- ============================================
-- Student Management System - SQL Project
-- Author: Soni Govindu
-- ============================================

* Create Database
CREATE DATABASE stu_mgmt;
USE stu_mgmt;

* Create Students Table
CREATE TABLE students (
    student_id INT AUTO_INCREMENT PRIMARY KEY,
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50),
    gender VARCHAR(10),
    dob DATE,
    course VARCHAR(50),
    email VARCHAR(100) UNIQUE,
    phone VARCHAR(15),
    admission_date DATE,
    marks DECIMAL(5,2)
);

* Insert Sample Data
INSERT INTO students 
(first_name, last_name, gender, dob, course, email, phone, admission_date, marks)
VALUES
('Rahul', 'Sharma', 'Male', '2002-05-10', 'BSc IT', 'rahul@gmail.com', '9876543210', '2023-06-01', 88.00),
('Sneha', 'Patil', 'Female', '2001-08-15', 'BSc IT', 'sneha@gmail.com', '9123456780', '2023-06-01', 90.75),
('Soni', 'Govindu', 'Female', '2003-05-10', 'BSc CS', 'soni@gmail.com', '9876543210', '2023-06-01', 89.50);

* View All Students
SELECT * FROM students;

* Update Example
UPDATE students
SET marks = 88.00
WHERE student_id = 1;

* Delete Example
DELETE FROM students
WHERE student_id = 3;

* Aggregate Functions
SELECT AVG(marks) AS average_marks FROM students;

SELECT MAX(marks) AS highest_marks,
       MIN(marks) AS lowest_marks
FROM students;

* Group By
SELECT course, COUNT(*) AS total_students
FROM students
GROUP BY course;

* Subquery: Students Above Average
SELECT *
FROM students
WHERE marks > (SELECT AVG(marks) FROM students);

* Order By
SELECT first_name, marks
FROM students
ORDER BY marks DESC;

* Create View
CREATE VIEW top_students AS
SELECT first_name, last_name, marks
FROM students
WHERE marks > 85;

SELECT * FROM top_students
