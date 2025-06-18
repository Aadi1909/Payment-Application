# Payment Application

A modular, microservices-based payment application designed for secure and scalable digital transactions.  
This project includes user management, transaction processing, wallet operations, notifications, and service registration, built using Java Spring Boot (Maven).

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Getting Started](#getting-started)
- [Service Descriptions](#service-descriptions)
- [License](#license)

---

## Overview

This repository provides the foundation for a digital payment platform consisting of independent services, each responsible for core aspects of a payment ecosystem. The project is organized for extensibility, reliability, and ease of deployment in a cloud-native environment.

---

## Features

- **User Service:** User registration, authentication, and management
- **Wallet Service:** Digital wallet creation and balance management
- **Transaction Service:** Secure and traceable money transfer between wallets
- **Notification Service:** Send notifications for transactions and events
- **Service Register:** Service discovery and registration for microservice communication
- **Microservices Architecture:** Decoupled services for scalability and maintainability
- **Spring Boot + Maven:** Robust Java backend stack

---

## Project Structure

```
payment-application/
└── Application/
    ├── notification-service/   # Handles user and system notifications
    ├── service-register/       # Service registration/discovery (e.g., Eureka, Consul)
    ├── transaction-service/    # Core transaction logic and APIs (Spring Boot/Maven)
    ├── user-service/           # User authentication and management
    └── wallet-service/         # Digital wallet management
```

---

## Getting Started

### Prerequisites

- Java 17+ (recommended)
- Maven 3.8+
- (Optional) Docker for containerized deployments

### Running Services

Each service can be built and run independently:

```bash
cd Application/<service-name>
mvn spring-boot:run
```

Replace `<service-name>` with one of:
- `user-service`
- `wallet-service`
- `transaction-service`
- `notification-service`
- `service-register`

Services typically start on different ports (see each service's application.properties).

### Building all services

You can build all services (sequentially):

```bash
cd Application
for d in */ ; do
  cd "$d"
  mvn clean install
  cd ..
done
```

---

## Service Descriptions

- **user-service:**  
  Handles user sign up, login, profile management, and authentication.

- **wallet-service:**  
  Manages wallet creation, balance checks, and updates for users.

- **transaction-service:**  
  Processes fund transfers, transaction history, and ensures atomicity and consistency.

- **notification-service:**  
  Sends users notifications (email/SMS/push) about transactions or important events.

- **service-register:**  
  Provides service registration and discovery to enable communication between microservices.

---

## License

MIT

---

*For questions, suggestions, or contributions, please create an issue or submit a pull request!*
