# Web Application Development – Lab 4  
## Student Management System (JSP + MySQL)

---

# VIETNAM NATIONAL UNIVERSITY – HO CHI MINH CITY  
## INTERNATIONAL UNIVERSITY  

---

## Course Information
- **Course:** Web Application Development  
- **Instructor:** Tran Khai Minh  
- **Lab:** Lab 4 – JSP + MySQL CRUD Operations  

---

## Student Information
- **Full Name:** Phạm Thanh Thư  
- **Student ID:** ITCSIU24083  
- **Date Submitted:** 28/04/2026  

---

# 1. PROJECT OVERVIEW

This project implements a **Student Management System** using **Java Server Pages (JSP)** and **MySQL database**.

The system provides full **CRUD functionality** and additional features such as:
- Search students by name or code  
- Input validation (email, student code format)  
- Pagination for large datasets  
- Improved user interface and experience  

All database interactions are handled securely using **JDBC with PreparedStatement**.

---

#  2. OBJECTIVES

The main objectives of this lab are:
- Connect JSP pages to MySQL using JDBC  
- Implement CRUD operations (Create, Read, Update, Delete)  
- Prevent SQL Injection using PreparedStatement  
- Handle form submissions and URL parameters  
- Implement server-side validation  
- Improve user experience with pagination and UI enhancements  

---

# 3. DATABASE DESIGN

## Table: `students`

| Column Name   | Data Type     | Description              |
|--------------|--------------|--------------------------|
| id           | INT (PK)     | Auto-increment ID        |
| student_code | VARCHAR      | Unique student code      |
| full_name    | VARCHAR      | Student full name        |
| email        | VARCHAR      | Email address (optional) |
| major        | VARCHAR      | Student major            |
| created_at   | TIMESTAMP    | Record creation time     |

---

# 4. SYSTEM FUNCTIONALITY

## 4.1 View Students
- Display all students in a table  
- Sorted by newest records  
- Includes Edit and Delete actions  

---

## 4.2 Add Student
- Form input with validation  
- Required fields: Student Code, Full Name  
- Inserts data into database using PreparedStatement  

---

##  4.3 Edit Student
- Pre-filled form with existing data  
- Student code is read-only  
- Updates database record using ID  

---

##  4.4 Delete Student
- Deletes record by ID  
- Confirmation dialog before deletion  
- Redirects with success/error message  

---

#  5. SEARCH FUNCTIONALITY

- Search by **student name** or **student code**  
- Uses SQL `LIKE` operator  
- Implemented with GET method (URL-based search)  

Example query:
```sql
SELECT * FROM students 
WHERE full_name LIKE ? OR student_code LIKE ?
