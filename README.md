# Skill-Based Task Allocation

A full-stack task management application that intelligently allocates tasks to employees based on their skills and availability. The system provides separate workflows for managers and employees, with secure authentication, task lifecycle management, and automated end-to-end testing.

## 🚀 Overview

Skill-Based Task Allocation is designed to simplify task assignment within teams by matching tasks with employees who have the required skills.

Managers can create and manage tasks, while employees can view their assigned tasks, update their progress, manage their skills, and control their availability.

The project also includes a dedicated Selenium + TestNG automation suite following the **Page Object Model (POM)** design pattern for reliable UI testing.

## ✨ Key Features

### 👨‍💼 Manager

* Secure manager authentication
* Create and manage tasks
* Specify required skills for tasks
* Automatic skill-based employee allocation
* View task assignment and status
* Monitor task progress

### 👨‍💻 Employee

* Secure employee login
* View assigned tasks
* Update task status
* Manage personal skills
* Toggle availability
* Track assigned work through the task lifecycle

### 🧠 Skill-Based Allocation

The system evaluates employee skills and availability when assigning tasks, helping managers allocate work to suitable team members instead of relying entirely on manual assignment.

### 🧪 Automated Testing

The project includes an independent Selenium automation module using:

* Selenium WebDriver
* TestNG
* Page Object Model (POM)
* WebDriverManager
* Maven

Automated scenarios cover authentication, signup, task creation, automatic allocation, employee task progression, profile management, and negative test cases.

## 🛠️ Tech Stack

### Frontend

* Angular 17
* TypeScript
* HTML
* CSS
* RxJS

### Backend

* Java 17
* Spring Boot 3.2
* Spring Web
* Spring Data JPA
* Hibernate
* MySQL
* JWT
* Maven
* Lombok

### Testing

* Selenium 4
* TestNG
* WebDriverManager
* Maven
* Page Object Model

## 📁 Project Structure

```text
Skill-Based-Task-Allocation/
│
├── backend/
│   ├── src/
│   └── pom.xml
│
├── frontend/
│   ├── src/
│   ├── angular.json
│   └── package.json
│
├── selenium-testing/
│   ├── src/test/
│   ├── testng.xml
│   ├── pom.xml
│   └── run-tests.ps1
│
├── .gitignore
└── README.md
```

## ⚙️ Prerequisites

Make sure the following are installed:

* Java 17 or higher
* Maven
* Node.js and npm
* Angular CLI
* MySQL
* Google Chrome
* Git

## 🔧 Setup & Installation

### 1. Clone the Repository

```bash
git clone https://github.com/avi-jain-26/Skill-Based-Task-Allocation.git
cd Skill-Based-Task-Allocation
```

### 2. Configure MySQL

Create a MySQL database and configure the database credentials in the Spring Boot application's configuration.

Update the database URL, username, and password according to your local MySQL setup.

### 3. Start the Backend

```bash
cd backend
mvn spring-boot:run
```

The backend runs on:

```text
http://localhost:8081
```

### 4. Start the Frontend

Open another terminal:

```bash
cd frontend
npm install
npm start
```

The Angular application runs on:

```text
http://localhost:4200
```

## 🧪 Running Automated Tests

The Selenium automation project is located inside `selenium-testing`.

```bash
cd selenium-testing
mvn test
```

### Run Smoke Tests

```bash
mvn test -DsuiteXmlFile=smoke-suite.xml
```

### Run a Specific Test Class

```bash
mvn test -Dtest=LoginTest
```

### Run a Specific Test Method

```bash
mvn test "-Dtest=LoginTest#managerCanLogIn"
```

### Run Tests by Group

```bash
mvn test -Dgroups=smoke
```

## 📋 Test Coverage

| Test Module      | Coverage                                               |
| ---------------- | ------------------------------------------------------ |
| LoginTest        | Login, page loading and negative login scenarios       |
| SignupTest       | Employee/manager signup and duplicate email validation |
| ManagerTaskTest  | Task creation and automatic allocation                 |
| EmployeeTaskTest | Task lifecycle from assignment to completion           |
| ProfileTest      | Skill management and availability                      |

## 🏗️ Testing Architecture

The Selenium test suite follows the **Page Object Model (POM)** architecture.

```text
Tests
  │
  ├── LoginTest
  ├── SignupTest
  ├── ManagerTaskTest
  ├── EmployeeTaskTest
  └── ProfileTest
          │
          ▼
     Page Objects
          │
          ▼
    Selenium WebDriver
          │
          ▼
     SkillTask Application
```

This approach separates page interactions from test logic, making the test suite easier to maintain and extend.

## 📊 Test Reports

After executing the test suite, reports can be generated in:

```text
test-output/index.html
target/surefire-reports/emailable-report.html
```

## 🔑 Demo Credentials

The application includes seeded demo accounts for testing.

| Role     | Email                                       | Password    |
| -------- | ------------------------------------------- | ----------- |
| Manager  | [manager@demo.com](mailto:manager@demo.com) | password123 |
| Employee | [alice@demo.com](mailto:alice@demo.com)     | password123 |
| Employee | [bob@demo.com](mailto:bob@demo.com)         | password123 |
| Employee | [charlie@demo.com](mailto:charlie@demo.com) | password123 |

## 🎯 Project Goals

* Automate skill-based task assignment
* Improve team workload distribution
* Reduce manual task allocation
* Provide clear task progress tracking
* Maintain secure role-based access
* Demonstrate full-stack development and automated testing practices

## 🔮 Future Enhancements

* Advanced task prioritization
* Improved employee workload balancing
* Real-time notifications
* Dashboard analytics
* Docker-based deployment
* CI/CD integration for automated testing

## 👨‍💻 Author

**Ayushi Gupta**

GitHub: [Ayushi240](https://github.com/Ayushi240/Skill-Based-Task-Allocation-.git)

---

⭐ If you find this project useful, consider giving it a star!
