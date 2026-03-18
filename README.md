# ✈️ Airport Cache System (Spring Boot)

> A backend system demonstrating caching mechanisms in an airport-related service using Spring Boot.

---

## 🚀 Introduction

**Airport Cache System** is a backend project designed to demonstrate how caching works in a real-world application.

The system simulates airport-related data (such as flights, routes, or locations) and applies caching techniques to improve performance and reduce database load.

This project helps understand:

* How caching improves response time
* How to integrate cache into Spring Boot
* How to optimize backend performance

---

## 🛠️ Tech Stack

* **Backend:** Java (Spring Boot)
* **Cache:** Redis / In-memory Cache (depending on your setup)
* **Database:** MySQL / H2 (if used)
* **Build Tool:** Maven
* **API Testing:** Postman

---

## 🧱 Architecture

The project follows a layered architecture:

* **Controller:** Handle API requests
* **Service:** Business logic + caching logic
* **Repository:** Data access
* **Cache Layer:** Store frequently accessed data

---

## 📂 Project Structure

```bash
📦 Airport_Cache
 ┣ 📂 controller     # API endpoints
 ┣ 📂 service        # Business logic + caching
 ┣ 📂 repository     # Data access
 ┣ 📂 entity         # Data models
 ┣ 📂 config         # Cache configuration
 ┣ 📂 resources
 ┃ ┗ 📜 application.properties
 ┗ 📜 pom.xml
```

---

## ⚙️ Installation & Setup

### 1. Clone project

```bash
git clone https://github.com/thiennguyenk01/Airport_Cache.git
cd Airport_Cache
```

---

### 2. Configure application

Edit `application.properties`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/airport_cache
spring.datasource.username=root
spring.datasource.password=

# Cache config (example)
spring.cache.type=simple
```

---

### 3. Install dependencies

```bash
mvn clean install
```

---

### 4. Run application

```bash
mvn spring-boot:run
```

👉 Server runs at: **http://localhost:8080**

---

## 📡 API Example

| Method | Endpoint           | Description                |
| ------ | ------------------ | -------------------------- |
| GET    | /api/airports      | Get all airports           |
| GET    | /api/airports/{id} | Get airport by ID (cached) |

---

## ⚡ Caching Mechanism

* First request → fetch from database
* Subsequent requests → return from cache
* Improves performance and reduces DB queries

---

## 🎯 Features

* ⚡ Caching implementation (Spring Cache / Redis)
* 📡 RESTful API
* 🧩 Clean architecture
* 🚀 Performance optimization demo

---

## 📌 Future Improvements

* 🔐 Add authentication (Spring Security + JWT)
* 📊 Cache monitoring (Redis UI)
* 🔄 Cache eviction strategies
* 🌐 Deploy with Docker

---
