# Inventory Management API

A secure and scalable Inventory Management REST API built using Spring Boot, Spring Security, JWT Authentication, Hibernate, and MySQL.

This project demonstrates backend development skills including RESTful API design, secure authentication, role-based authorization, database management, exception handling, validation, and API documentation.

---

## Features

### Authentication & Authorization
- User Registration
- User Login
- JWT Token Generation
- JWT Token Validation
- Role-Based Access Control (`ADMIN` / `STAFF`)

### Category Management
- Create Category
- Update Category
- Delete Category
- View Categories

### Product Management
- Create Product
- Update Product
- Delete Product
- Get Product by ID
- List All Products

### Dashboard Analytics
- Total Products Count
- Total Categories Count
- Total Inventory Value

### Additional Features
- Request Validation
- Global Exception Handling
- API Documentation with Swagger
- MySQL Database Integration

---

## Tech Stack

| Technology | Usage |
| :--- | :--- |
| **Java 21** | Programming Language |
| **Spring Boot** | Backend Framework |
| **Spring Security** | Authentication & Authorization |
| **JWT** | Stateless Authentication |
| **Spring Data JPA** | Data Access Layer |
| **Hibernate** | ORM Framework |
| **MySQL** | Relational Database |
| **Maven** | Dependency Management |
| **Lombok** | Boilerplate Reduction |
| **Swagger/OpenAPI** | API Documentation |
| **Postman** | API Testing |
| **Git & GitHub** | Version Control |

---

## Project Structure

```text
src
├── main
│   ├── java
│   │   └── com.hhnv.inventory
│   │       ├── controller
│   │       ├── service
│   │       ├── repository
│   │       ├── entity
│   │       ├── dto
│   │       ├── security
│   │       ├── exception
│   │       └── config
│   │
│   └── resources
│       └── application.properties
│
└── test
```

---

## Database Design

### User                                
| Field | Type |
| :--- | :--- |
| `id` | `Long` |
| `username` | `String` |
| `email` | `String` |
| `password` | `String` |
| `role` | `ADMIN` / `STAFF` |



### Product
| Field | Type |
| :--- | :--- |
| `id` | `Long` |
| `name` | `String` |
| `description` | `String` |
| `price` | `Double` |
| `quantity` | `Integer` |
| `category_id` | `Long` |

---

## API Endpoints

### Authentication
| Method | Endpoint |
| :--- | :--- |
| `POST` | `/api/auth/register` |
| `POST` | `/api/auth/login` |

### Categories
| Method | Endpoint |
| :--- | :--- |
| `GET` | `/api/categories` |
| `POST` | `/api/categories` |
| `PUT` | `/api/categories/{id}` |
| `DELETE` | `/api/categories/{id}` |

### Products
| Method | Endpoint |
| :--- | :--- |
| `GET` | `/api/products` |
| `GET` | `/api/products/{id}` |
| `POST` | `/api/products` |
| `PUT` | `/api/products/{id}` |
| `DELETE` | `/api/products/{id}` |

### Dashboard
| Method | Endpoint |
| :--- | :--- |
| `GET` | `/api/dashboard/total-products` |
| `GET` | `/api/dashboard/total-categories` |
| `GET` | `/api/dashboard/inventory-value` |

---

## Getting Started

### 1. Clone Repository
```bash
git clone https://github.com/YOUR_USERNAME/inventory-management-api.git
```

### 2. Navigate to Project
```bash
cd inventory-management-api
```

### 3. Create Database
```sql
CREATE DATABASE inventory_db;
```

### 4. Configure Database
Update `src/main/resources/application.properties`:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/inventory_db
spring.datasource.username=root
spring.datasource.password=your_password
spring.jpa.hibernate.ddl-auto=update
```

### 5. Run Application
```bash
mvn spring-boot:run
```
The application will start on: `http://localhost:8080`

---

## Future Enhancements

- [ ] Product Search
- [ ] Pagination & Sorting
- [ ] Inventory Reports
- [ ] Low Stock Alerts
- [ ] Docker Support
- [ ] Unit & Integration Testing
- [ ] CI/CD Pipeline using GitHub Actions

---

## Author

**Hiriwaddala Hewage Nethsara Vimukthi Induwara**  
*3rd Year BSc (Hons) Computer Science Undergraduate — NSBM Green University*

**Focus Areas:**
- Java & Spring Boot
- Backend Development
- REST APIs
- Database Systems

**Connect:**
- **LinkedIn:** www.linkedin.com/in/hhnethsara
- **GitHub:** https://github.com/hhnethsara