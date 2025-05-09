# Spring Cloud API Gateway – Static Routing (No Eureka)

This project demonstrates how to use **Spring Cloud Gateway** as an API Gateway **without using Eureka or any service registry**. Instead, it uses **static route configuration** in `application.yml` to forward requests to backend microservices.

---

## 🔧 Features

- Spring Cloud Gateway without Eureka
- Static route definitions (manual config)
- Simple routing using path predicates
- upports forwarding to multiple services
- Easily extendable for filters, CORS, rate limiters



---

## 🚀 Getting Started

### Prerequisites

- Java 17+
- Maven 3.6+
- Backend microservices running on different ports (e.g., `user-service` on 8081, `order-service` on 8082)


# Step 1: Build the application
mvn clean install

# Step 2: Run the application
mvn spring-boot:run

# Sample API Calls
curl http://localhost:8080/user/profile
Forwarded to: http://localhost:8081/user/profile

curl http://localhost:8080/order/summary
Forwarded to: http://localhost:8082/order/summary

