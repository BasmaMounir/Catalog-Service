# Catalog Service (E‑Commerce Microservice)

This is the **Catalog Microservice** responsible for managing products and categories within a modular e‑commerce system. It is designed to follow **clean architecture principles**, and communicates with other services like User Service.

## 🧩 Key Features

- **CRUD operations** for Product and Category entities
- Connects with **User Service** via **WebClient** for authentication and user validation
- Uses **Spring Cloud Eureka** for service discovery
- Routed through **Spring Cloud Gateway**
- Structured for **clean code and scalability**

## ⚙️ Technologies Used

- **Java 17**
- **Spring Boot**
- **Spring Data JPA**
- **MySQL**
- **Spring Cloud (Eureka, Gateway)**
- **WebClient** (REST communication)
- **Lombok**
- **Docker** support

## 📁 Project Structure

```
src/
├── controller/       # ProductController, CategoryController
├── model/            # Product, Category entities
├── repository/       # JPA Repositories
├── service/          # Business logic
├── config/           # WebClient config, etc.
```

## 🔌 API Endpoints (Sample)

- `GET /products` – Get all products  
- `GET /products/{id}` – Get product by ID  
- `POST /products` – Create product  
- `PUT /products/{id}` – Update product  
- `DELETE /products/{id}` – Delete product  
- Similar endpoints for `/categories`

## 🔐 Inter-service Communication

- Uses **WebClient** to communicate with User Service for checking user roles/authorization.
- Authenticated requests include JWT in `Authorization` header.

## 🚀 Deployment

✅ Deployed on **[Railway](https://railway.app/)** and integrated with other microservices (User, Notification, etc).

## 📦 Docker Support

Fully Dockerized and can be run in isolation or within a Docker Compose setup.
## 🐳 Docker Image
Pull the latest Catalog Service image from Docker Hub:
```bash
docker pull basmamounir/catalogservice:latest
```
