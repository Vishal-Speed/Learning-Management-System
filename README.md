# Learning Management System Backend

## Overview
The **Learning Management System (LMS) Backend** is a Spring Boot-based RESTful API designed to power an educational platform. It enables management of users, courses, enrollments, and learning progress, with a focus on scalability, security, and maintainability.

## Features
- ✅ **JWT-Based Authentication & Authorization**
- 🔐 **Role-Based Access Control** (ADMIN, INSTRUCTOR, STUDENT)
- 📚 **Course & Enrollment Management**
- 📈 **Progress Tracking** (Lessons, completions)
- ⚠️ **Global Exception Handling**
- 🌐 **RESTful API Design (HTTP Status Codes, DTOs)**

## Tech Stack
| Category         | Technology           |
|------------------|----------------------|
| **Backend**      | Java 21, Spring Boot |
| **Database**     | MySQL                |
| **Security**     | Spring Security, JWT |
| **Build Tool**   | Maven                |
| **Architecture** | Monolithic           |

## Project Structure
```
LMS-Backend/
├── src/
│   ├── main/
│   │   ├── java/com/lms/
│   │   │   ├── config/         # Configuration (Security, JWT, etc.)
│   │   │   ├── controller/     # REST Controllers
│   │   │   ├── dto/            # Data Transfer Objects
│   │   │   ├── exception/      # Custom Exceptions & Handlers
│   │   │   ├── mapper/         # DTO ↔ Entity Mappers
│   │   │   ├── model/          # JPA Entities
│   │   │   ├── repository/     # Spring Data Repositories
│   │   │   ├── security/       # Spring Security & JWT Logic
│   │   │   ├── service/        # Business Logic Layer
│   │   │   ├── startup/        # Data Initialization
│   │   │   └── LMSBackendApplication.java
│   └── test/                   # Unit & Integration Tests
├── pom.xml                     # Maven Dependencies
├── .gitignore                  # Git Ignore Rules
├── README.md                   # Project Documentation
```

## Installation & Setup

### ✅ Prerequisites
- Java 17 or higher
- Maven
- MySQL Server
- Git

### ⚙️ Setup Steps
1. **Clone the repository**
   ```bash
   git clone https://github.com/VishalNarsinh/Learning-Management-System.git
   cd Learning-Management-System
   ```

2. **Configure MySQL database**
   - Update `src/main/resources/application.properties` with your MySQL credentials.

3. **Build the project**
   ```bash
   mvn clean install
   ```

4. **Run the application**
   ```bash
   mvn spring-boot:run
   ```

## Sample `application.properties` Configuration

```properties
# Server Configuration
server.port=8080

# Database Configuration
spring.datasource.url=jdbc:mysql://localhost:3306/lms
spring.datasource.username=root
spring.datasource.password=your_password
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

# Hibernate Configuration
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect

# JWT Configuration (example values)
app.jwt.secret=your_jwt_secret_key
app.jwt.expiration=86400000
```

## Contributing
Contributions are welcome!  
If you find a bug or want to add a new feature, feel free to fork this repository and submit a pull request.

## Contact
- 👨‍💻 **Developer**: Vishal Narsinh
- 🌐 **GitHub**: [@VishalNarsinh](https://github.com/VishalNarsinh)
- 📧 **Email**: [vishalnarsinh@gmail.com](mailto:vishalnarsinh@gmail.com)

- making changes
