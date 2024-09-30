# 🚗 Car Rental System

### A Comprehensive Full-Stack Application for Managing a Car Rental Business

---

## 📋 Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Database Schema](#database-schema)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Custom Exceptions](#custom-exceptions)
- [Unit Testing](#unit-testing)
- [Contributing](#contributing)
- [License](#license)

---

## 📖 Project Overview

The **Car Rental System** is a full-stack web/mobile application designed to manage a car rental business. The system includes features for managing cars, customers, leases, and payments. This project focuses on the use of object-oriented programming, database interaction via SQL, control flow statements, loops, exception handling, and unit testing.

---

## ✨ Features

- **Customer Management**: Add, update, and retrieve customer details.
- **Car Management**: Add new cars, update availability, and view available/rented cars.
- **Lease Management**: Create daily or monthly leases and calculate lease costs.
- **Payment Handling**: Record payments and retrieve payment history.
- **Exception Handling**: Handles custom exceptions for invalid operations.
- **Unit Testing**: Includes tests to ensure system correctness and reliability.

---

## 🛠 Technologies Used

- **Java** (Backend)
- **MySQL** (Database)
- **JDBC** (Database Connectivity)
- **JUnit** (Testing)
- **Maven** (Build Automation)
- **Spring Boot** (Optional: For creating REST APIs)
- **Frontend**: HTML, CSS, JavaScript (for web app) or Android Studio (for mobile app)

---

## 🗄 Database Schema

The system uses the following SQL schema:

1. **Vehicle Table**:
   - `vehicleID` (Primary Key)
   - `make`, `model`, `year`, `dailyRate`
   - `status` (available/notAvailable)
   - `passengerCapacity`, `engineCapacity`

2. **Customer Table**:
   - `customerID` (Primary Key)
   - `firstName`, `lastName`, `email`, `phoneNumber`

3. **Lease Table**:
   - `leaseID` (Primary Key)
   - `vehicleID` (Foreign Key)
   - `customerID` (Foreign Key)
   - `startDate`, `endDate`, `type` (Daily/Monthly)

4. **Payment Table**:
   - `paymentID` (Primary Key)
   - `leaseID` (Foreign Key)
   - `paymentDate`, `amount`

---

## 📁 Project Structure

```bash
src/
  ├── entity/model
  │     ├── Car.java
  │     ├── Customer.java
  │     ├── Lease.java
  │     ├── Payment.java
  ├── dao
  │     ├── ICarLeaseRepository.java
  │     ├── ICarLeaseRepositoryImpl.java
  ├── exception
  │     ├── CarNotFoundException.java
  │     ├── CustomerNotFoundException.java
  │     ├── LeaseNotFoundException.java
  ├── util
  │     ├── DBPropertyUtil.java
  │     ├── DBConnUtil.java
  ├── main
  │     ├── MainModule.java
  ├── test
  │     ├── CarRentalTest.java

```



## 🚀 Getting Started

### Prerequisites
- Java 11+
- MySQL
- Maven
- JDBC Driver for MySQL
- JUnit for testing

### 🛠 Usage
After running the application, use the console or frontend to navigate through the following menu options:

#### Customer Management:
- Add, update, and list customers.

#### Car Management:
- Add, update, and view cars.

#### Lease Management:
- Create and manage car leases.

#### Payment Handling:
- Record and view payments.

## 📊 API Endpoints (For REST API)
*(Optional for Spring Boot-based applications)*

- `POST /cars`: Add a new car.
- `GET /cars/available`: List available cars.
- `POST /leases`: Create a new lease.
- `POST /payments`: Record a payment.

## 🚨 Custom Exceptions
- **CarNotFoundException**: Thrown when a car ID doesn't exist in the database.
- **LeaseNotFoundException**: Thrown when a lease ID doesn't exist.
- **CustomerNotFoundException**: Thrown when a customer ID doesn't exist.

## ✅ Unit Testing
Unit tests are included to ensure system correctness. Key tests include:
- Car creation success test.
- Lease creation and retrieval tests.
- Exception handling tests for invalid IDs.


