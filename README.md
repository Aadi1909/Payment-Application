# Payment Application

## Overview
The **Payment Application** is a secure and efficient platform designed for handling financial transactions. Built with **Spring Boot**, this application provides seamless payment processing, transaction management, and integration with external payment gateways.

## Features
- **User Authentication & Authorization**: Secure login and role-based access control.
- **Transaction Processing**: Reliable payment gateway integration for seamless transactions.
- **Payment History & Tracking**: Keep track of past transactions with detailed logs.
- **Refund & Dispute Management**: Handle refunds and disputes efficiently.
- **Admin Dashboard**: Manage users, transactions, and system configurations.

## Tech Stack
- **Backend**: Spring Boot, Java, Hibernate, Lombok
- **Database**: PostgreSQL/MySQL
- **Security**: Spring Security, JWT Authentication
- **API Documentation**: Swagger
- **Build Tool**: Maven/Gradle

## Installation
### Prerequisites
- Java 17+
- Maven/Gradle
- PostgreSQL/MySQL

### Steps
1. Clone the repository:
   ```sh
   git clone https://github.com/Aadi1909/Payment-Application.git
   cd Payment-Application/Application
   ```
2. Configure the database in `application.properties`:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/payment_db
   spring.datasource.username=root
   spring.datasource.password=yourpassword
   ```
3. Build and run the application:
   ```sh
   mvn clean install
   mvn spring-boot:run
   ```

## API Endpoints
| Method | Endpoint | Description |
|--------|---------|-------------|
| POST | `/api/auth/register` | Register a new user |
| POST | `/api/auth/login` | Authenticate and obtain JWT |
| GET | `/api/payments/{id}` | Get payment details |
| POST | `/api/payments` | Process a new payment |
| PUT | `/api/payments/refund/{id}` | Initiate a refund |

## Contribution Guidelines
1. Fork the repository.
2. Create a new branch for your feature: `git checkout -b feature-name`
3. Commit your changes: `git commit -m "Added new feature"`
4. Push to the branch: `git push origin feature-name`
5. Open a Pull Request.

## License
This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

## Contact
For any queries, reach out to **Aadarsh Tyagi** via [GitHub](https://github.com/Aadi1909).

