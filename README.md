------------------------DAY-01-------------------------------------------
CRM
-CRM is defined as the Customer Relationship Management..
A software used to manage customers and business operations.
WHY COMPANIES USE SALESFORCCE?
Companies use Salesforce because it helps them to:
- store customer data
- track sales
- improve customer support
- automate work
- manage business easily
EXPLAIN------
1.ACCOUNT
Account is used to store company or organization details.
Ex: Infosys, TCS
2.CONTACT
Contact means a person related to an account.
Ex:customer or employee
3.OPPORTUNITY
Opportunity means a possible business deal or sale.
ex:customer interested in buying a product

REAL WORLD MAPPING
College Management System

| Salesforce Concept | Real Example |
|---|---|
| Account | College |
| Contact | Student |
| Opportunity | Student Admission |<img width="1858" height="787" alt="Screenshot 2026-05-08 205950" src="https://github.com/user-attachments/assets/4a2630ed-9117-4978-bad7-eba7df7456dd" />
------------------------------------DAY-02------------------------------------
# Salesforce CRM Project

## What is Salesforce Platform?
Salesforce is a cloud-based CRM platform used for managing customer relationships, sales, automation, and application development.

---

## Concepts

### App
Collection of tabs and objects for a business process.

### Object
Database table used to store records.

### Tab
Navigation item used to open objects/features.

---

## Configuration vs Coding

| Configuration | Coding |
|---|---|
| Click-based | Programming-based |
| Easy customization | Advanced logic |

---

## System Design

### Standard Objects
- Account
- Contact
- Opportunity

### Custom Objects
- Property
- Offer

### Relationships
- Offer → Property (Master-Detail)
- Offer → Contact (Lookup)

---

## Features Implemented
- Validation Rules
- Formula Fields
- Roll-Up Summary Fields
- Dynamic Forms
- Field Dependencies
- Lightning Record Pages

---

## Screenshots
<img width="1910" height="760" alt="Screenshot 2026-05-18 114438" src="https://github.com/user-attachments/assets/be353a29-1fdd-4075-9fd2-64de7fe3970b" />
<img width="1898" height="762" alt="Screenshot 2026-05-18 114415" src="https://github.com/user-attachments/assets/6e337f24-af68-435b-be91-485472dbafa3" />
<img width="1906" height="768" alt="Screenshot 2026-05-16 210856" src="https://github.com/user-attachments/assets/86c1beea-953f-44a3-a148-322d3f6bbbaf" />
<img width="1885" height="763" alt="Screenshot 2026-05-16 210833" src="https://github.com/user-attachments/assets/fcc14d43-7c09-464e-91f9-119cfc3b0d89" />
<img width="1858" height="787" alt="Screenshot 2026-05-08 205950" src="https://github.com/user-attachments/assets/88e66db3-04d7-4257-9cd4-4f370ca39dd6" />
--------------------------------DAY-03---------------------------------------
# Day 3 – Data Modeling in Salesforce

## 1. Difference Between App, Object, Record, and Field

| Term | Description | Example |
|------|-------------|----------|
| App | A collection of tools, tabs, and objects designed for a specific business purpose | College Management App |
| Object | A database table that stores related data | Student Object |
| Record | A single entry inside an object | One student’s details |
| Field | A column in an object used to store specific information | Student Name, Roll Number |

---

# 2. Standard vs Custom Objects

| Standard Objects | Custom Objects |
|------------------|----------------|
| Already provided by Salesforce | Created by users |
| Used for common business needs | Used for specific requirements |
| Examples: Account, Contact, Opportunity | Examples: Student, Faculty, Course |
| Cannot be deleted easily | Can be customized and deleted |

---

# 3. College Data Model

## Objects

### Standard Objects
- Account
- Contact

### Custom Objects
- Student
- Faculty
- Course
- Department
- Attendance

---

## Relationships

| Parent Object | Child Object | Relationship Type |
|----------------|--------------|-------------------|
| Department | Faculty | One-to-Many |
| Department | Course | One-to-Many |
| Course | Student | Many-to-Many |
| Student | Attendance | One-to-Many |

---

## Data Model Diagram

```text
Department
   |
   |---- Faculty
   |
   |---- Course
              |
              |---- Student
                          |
                          |---- Attendance
```

---

# 4. Formula Fields

Formula fields automatically calculate values based on other fields.

## Example 1: Student Full Name

```text
First_Name + " " + Last_Name
```

### Explanation
This formula combines first name and last name into a single field.

---

## Example 2: Attendance Percentage

```text
(Classes_Attended / Total_Classes) * 100
```

### Explanation
This calculates the attendance percentage of a student.

---

# 5. Validation Rules

Validation rules prevent incorrect data from being saved.

## Example 1: Phone Number Validation

```text
LEN(Phone_Number) != 10
```

### Explanation
Ensures the phone number contains exactly 10 digits.

---

## Example 2: Age Validation

```text
Age < 17
```

### Explanation
Prevents students younger than 17 from being added.

---

# 6. Reflection – Why Structured Enterprise Data Matters

Structured enterprise data is important because it helps organizations store, manage, and analyze information efficiently. In a college management system, structured data helps maintain student records, attendance, faculty details, and course information accurately.

## Benefits
- Better organization of data
- Faster data retrieval
- Improved decision-making
- Reduced duplication and errors
- Easier reporting and analytics

Proper data modeling ensures scalability, consistency, and reliability in enterprise applications like Salesforce.

---

