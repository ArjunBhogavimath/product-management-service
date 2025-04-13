
# 📦 Product API - Spring Boot


A simple RESTful API built with Spring Boot to manage a list of products.

---

## 🚀 Features

- Create, Read, Update, and Delete (CRUD) operations on products
- RESTful API structure
- In-memory H2 database (or switch to PostgreSQL/MySQL easily)
- Clean architecture with controller, service, and repository layers

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
- Spring Boot
- Spring Data JPA
- H2 (or PostgreSQL/MySQL)
- Maven
- Postman (for API testing)

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
