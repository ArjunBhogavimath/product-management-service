
# 📦 Product API - Spring Boot


A simple RESTful API built with Spring Boot to manage a list of products.

---

## 🚀 Features

- Create, Read, Update, and Delete (CRUD) operations on products
- RESTful API structure
- In-memory H2 database (or switch to PostgreSQL/MySQL easily)
- Clean architecture with controller, service, and repository layers
- Input validation using `jakarta.validation`
- Centralized exception handling using `@RestControllerAdvice`
- API tested via Postman collection

---

## 📂 Folder Structure

```
product-service/
├── src/
│   └── main/
│       ├── java/com/edstruments/product_service/
│       │   ├── controller/
│       │   ├── exception/
│       │   │   ├── GlobalExceptionHandler.java
│       │   │   └── ProductNotFoundException.java
│       │   ├── model/
│       │   ├── repository/
│       │   ├── service/
│       │   └── ProductServiceApplication.java
│       └── resources/
│           └── application.properties
├── docs/
│   └── Product-API-SpringBoot.postman_collection.json
├── README.md
└── pom.xml
```

---

## 🛠️ Tech Stack

- Java 17+
- Spring Boot 3.x
- Spring Data JPA
- H2 (or PostgreSQL/MySQL)
- Maven
- Jakarta Bean Validation (JSR-380)
- Postman (for API testing)

---


## 🧪 Input Validation

Validated using `@Valid` and `jakarta.validation.constraints`:

| Field     | Constraint                            |
|-----------|----------------------------------------|
| `name`    | `@NotBlank` – must not be blank        |
| `price`   | `@Positive` – must be a positive value |

### ❌ Sample Invalid Payload:

```json
{
  "name": "",
  "description": "Laptop",
  "price": -1200
}

```

## ✅ Response (400 Bad Request):
```json
{
  "name": "Name must not be blank",
  "price": "Price must be positive"
}
```

---

## ⚠️ Exception Handling

Custom exceptions handled by `@RestControllerAdvice`:

| Exception                        | When It Happens                               | HTTP Status |
|----------------------------------|-----------------------------------------------|-------------|
| `ProductNotFoundException`       | Product ID does not exist                     | 404         |
| `MethodArgumentNotValidException`| Input validation fails (invalid fields)       | 400         |
| `Exception` (generic fallback)   | Any unhandled exception                       | 500         |

### 🔍 Sample 404 Response:

```json
{
  "error": "Product with id 10 not found"
}
```

---


## 📥 Installation & Running

### 1. Clone the repository
```bash
git clone https://github.com/ArjunBhogavimath/product-management-service.git
cd product-service
```

### 2. Build and run the project
```bash
./mvnw spring-boot:run
```

or with Maven

```bash
mvn spring-boot:run
```

### 3. Access the API
```
Base URL: http://localhost:8080/api/products
```

---

## 🧪 API Testing

Use the provided Postman collection:

📁 [`docs/Product-API-SpringBoot.postman_collection.json`](docs/Product-API-SpringBoot.postman_collection.json)

---

## 📝 Example JSON Request (Create Product)

```json
{
  "name": "iPhone 15",
  "description": "Apple smartphone",
  "price": 1199.99
}
```

## Contact
**Mallikarjunaiah B M**  
vpmallikarjuna03@gmail.com  
[LinkedIn Profile](https://www.linkedin.com/in/mallikarjunaiah-b-m-1331a319a/)
