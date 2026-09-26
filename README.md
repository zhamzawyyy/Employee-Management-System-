# Employee Management System (EMS)

A desktop-based **Employee Management System** developed with **Java Swing** to manage employee information and common HR operations through separate Admin and Employee dashboards.

The system provides employee management, attendance tracking, leave management, and payroll processing with local file-based data persistence.

## Features

### Authentication

* Employee ID and password-based login.
* Separate access flow for administrators/managers and employees.
* Logout functionality.

### Admin Dashboard

Administrators can manage the main HR operations through a tabbed dashboard.

#### Employee Management

* Add employees.
* Edit employee information.
* Delete employees.
* View employee records.
* Manage departments, job roles, contact information, and hourly rates.

#### Attendance Tracking

* View employee attendance records.
* Track check-in and check-out times.
* Calculate working hours.
* View attendance information by employee.

#### Payroll Management

* Calculate payroll based on working hours and hourly rate.
* Calculate gross salary.
* Apply tax deductions.
* Calculate net salary.
* Manage payroll periods.

#### Leave Management

* View employee leave requests.
* Review pending requests.
* Approve or reject leave requests.
* Store comments related to leave decisions.

### Employee Dashboard

Employees can access their own dashboard to view and manage employee-related information, including:

* Profile information
* Attendance
* Leave requests
* Payroll information

## Technologies

* **Java**
* **Java Swing**
* **Object-Oriented Programming (OOP)**
* **Java Serialization**
* **Java Time API**
* **File-based persistence**

## Project Architecture

The project is organized around several Java classes responsible for different parts of the system:

```text
EMS/
│
├── EMS.java
├── LoginFrame.java
├── AdminDashboard.java
├── EmployeeDashboard.java
├── EmployeeDialog.java
│
├── DataManager.java
│
├── Employee.java
├── Attendance.java
├── Leave.java
├── LeaveStatus.java
├── Payroll.java
├── Department.java
└── UserRole.java
```

### Main Components

**EMS.java**

The main entry point of the application. It initializes the `DataManager` and launches the login interface.

**LoginFrame.java**

Handles employee authentication and redirects users to the appropriate dashboard.

**AdminDashboard.java**

Provides administrative functionality for employees, attendance, payroll, and leave management.

**EmployeeDashboard.java**

Provides employees with access to their own profile, attendance, leave requests, and related information.

**DataManager.java**

Acts as the main data-management layer. It handles employees, attendance records, leave requests, and payroll data and persists them using `.dat` files.

**Employee.java**

Represents an employee and stores information such as ID, name, email, phone number, department, job role, hourly rate, hire date, and password.

**Attendance.java**

Handles check-in/check-out records and calculates working hours.

**Leave.java**

Represents employee leave requests and their current status.

**Payroll.java**

Handles payroll calculations including working hours, gross salary, tax deductions, and net salary.

## Data Persistence

The application uses Java serialization to store data locally.

The main data files include:

```text
employees.dat
attendance.dat
leaves.dat
payroll.dat
```

This allows employee and HR data to remain available when the application is restarted.

## Departments

The system includes several departments:

* Human Resources
* Information Technology
* Finance
* Marketing
* Sales
* Operations
* Administration

## Payroll Calculation

Payroll is calculated using employee working hours and hourly rate.

The system also considers approved leave days when calculating expected working hours and applies the configured tax deduction before calculating the final net salary.

## Requirements

* Java JDK 8 or later
* IntelliJ IDEA or another Java IDE

## How to Run

### Using IntelliJ IDEA

1. Clone or download the repository.
2. Open the project in IntelliJ IDEA.
3. Make sure the Java SDK is configured.
4. Open:

```text
EMS.java
```

5. Run the `main()` method.

### Using the Terminal

Compile the Java files:

```bash
javac *.java
```

Then run:

```bash
java EMS
```

## Default Admin Account

The application creates a default administrator account when no employee data exists.

```text
Employee ID: 1000
Password: admin123
```

Change default credentials before using the project in a real environment.

## Purpose

This project demonstrates practical implementation of:

* Object-Oriented Programming
* Desktop GUI development
* Authentication and role-based access
* File-based data persistence
* Employee management
* Attendance tracking
* Leave management
* Payroll processing

It was developed as a practical Java application that combines multiple HR operations into one desktop system.
