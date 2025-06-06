# Tourism Management System

A comprehensive tourism management system built with Spring Boot and MVC architecture.

## Features

- User Management (Admin, Staff, Customer)
- Tour Management with detailed itineraries
- Booking System with payment integration
- Review and Rating System
- News and Blog Management
- File Upload and Management

## Technology Stack

- **Backend**: Spring Boot 3.2.5, Spring MVC, Spring Data JPA, Spring Security
- **Database**: SQL Server
- **Frontend**: Thymeleaf, Bootstrap 5, JavaScript
- **Build Tool**: Maven
- **Java Version**: 17+

## Getting Started

### Prerequisites

- Java JDK 17 or higher
- SQL Server
- Maven 3.6+
- Git

### Installation

1. Clone the repository:
```bash
git clone <your-repository-url>
cd travel-management
```

2. Configure database connection in `application-dev.properties`:
```properties
spring.datasource.url=jdbc:sqlserver://localhost:1433;databaseName=TourismManagement
spring.datasource.username=your_username
spring.datasource.password=your_password
```

3. Run the SQL script to create database and sample data

4. Build and run the application:
```bash
mvn clean install
mvn spring-boot:run
```

5. Access the application:
- Customer Portal: http://localhost:8080/tourism/
- Admin Panel: http://localhost:8080/tourism/admin
- API Documentation: http://localhost:8080/tourism/api

### Default Login Credentials

- **Admin**: admin / password
- **Customer**: customer01@gmail.com / password

## Project Structure

```
src/main/java/com/example/travel_management/
├── config/          # Configuration classes
├── controller/      # MVC Controllers
├── model/           # Entities, DTOs, Request/Response objects  
├── repository/      # Data access layer
├── service/         # Business logic layer
├── security/        # Security configuration
├── utils/           # Utility classes
├── exception/       # Exception handling
└── enums/           # Enumerations
```

## API Endpoints

### Authentication
- `POST /api/auth/login` - User login
- `POST /api/auth/register` - User registration

### Tours
- `GET /api/tours` - Get all tours
- `GET /api/tours/{id}` - Get tour by ID
- `POST /api/tours` - Create new tour (Admin only)

### Bookings
- `GET /api/bookings` - Get user bookings
- `POST /api/bookings` - Create new booking
- `PUT /api/bookings/{id}` - Update booking

## Contributing

1. Create a feature branch
2. Make your changes
3. Write tests
4. Submit a pull request

## License

This project is licensed under the MIT License.

## Contact

For questions or support, please contact [your-email@example.com]