# 🐾 VetCare – Distributed Veterinary Clinic Management System

**VetCare** is a distributed information management system for veterinary clinics, built with **Spring Cloud Microservices**. It automates daily clinic operations such as **customer management**, **veterinarian profiles**, and **pet appointment scheduling**.

---

## ✨ Features

* 👩‍⚕️ **Customer Service** – Manage pet owners and their pets (CRUD operations).
* 🩺 **Vets Service** – Store and manage veterinarian details and specialties.
* 📅 **Visits Service** – Schedule appointments and keep medical history.
* 🌐 **API Gateway** – Unified entry point for all services.
* 🔍 **Discovery Server (Eureka)** – Service registration and dynamic discovery.
* ⚙️ **Config Server** – Centralized configuration management.
* 🛠 **Scalability & Fault Isolation** – Independent scaling and deployment of each service.
* 💾 **Dedicated Databases** – Each microservice uses its own MySQL schema.

---

## 🏗 Architecture

VetCare follows a microservices-based modular architecture.
<img width="605" height="442" alt="image" src="https://github.com/user-attachments/assets/15556364-c54e-46e6-9538-0ada3c71fac3" />



Each service communicates through **REST APIs**, discovered dynamically via **Eureka**, and routed through the **API Gateway**.

---

## 🚀 Tech Stack

* **Backend:** Java, Spring Boot, Spring Cloud (Config, Eureka, Gateway)
* **Database:** MySQL (separate schema per service)
* **Frontend:** HTML, CSS, JavaScript (basic UI)
* **API Testing:** Postman
* **Version Control:** Git & GitHub

---

## ⚡ Setup & Deployment

### Prerequisites

* Java 17+
* Maven
* MySQL running locally
* Git

### Steps

1. **Clone the repository:**

   ```bash
   git clone https://github.com/YasinduDD/VetCare.git
   cd VetCare
   ```

2. **Start Config & Discovery Servers first:**

   ```bash
   cd config-server
   mvn spring-boot:run
   cd ../discovery-server
   mvn spring-boot:run
   ```

3. **Run core services (order doesn’t matter after discovery):**

   ```bash
   cd customer-service
   mvn spring-boot:run

   cd vets-service
   mvn spring-boot:run

   cd visits-service
   mvn spring-boot:run
   ```

4. **Start API Gateway:**

   ```bash
   cd api-gateway
   mvn spring-boot:run
   ```

5. **Access Application:**

   * API Gateway: `http://localhost:8080`
   * Eureka Dashboard: `http://localhost:8761`

---


👉 Do you also want me to add a **badges section** (e.g., Java version, build status, license) at the top for a more professional GitHub look?
