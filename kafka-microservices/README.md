# Kafka Microservices Project

This project demonstrates a **Spring Boot** and **Apache Kafka** microservices architecture with the following modules:

- **Order Service**
- **Email Service**
- **Stock Service**
- **Base Domain** (common/shared components)

---

## **Requirements**

To run the project locally, ensure you have the following installed:

- **Java 17**  
- **Maven**  
- **Gradle**  

---

## **Architecture Overview**

The project is designed using a **multi-layer architecture**, which is divided into the following layers:

### 1. **Presentation Layer**
This is the topmost layer of the architecture, responsible for handling communication with clients:

- **Authentication:** Verifies the identity of the user.
- **JSON Data Conversion:** Converts incoming JSON data into Java objects and vice versa.
- **Request Handling:** Manages incoming HTTP requests.
- **Authentication Transfer:** Transfers authentication data to the business layer for further validation.

### 2. **Business Layer**
This layer contains the core functionality and logic of the application:

- **Validation:** Ensures that the data is correct and meets the necessary requirements.
- **Authorization:** Manages access control to ensure that only authorized users can perform certain actions.
- **Business Logic:** Implements the core business rules and operations of the application.

### 3. **Persistence Layer**
This layer is responsible for managing interactions with the data storage system:

- **Storage Logic:** Contains the logic for data storage and retrieval.
- **Data Fetching:** Translates data into objects and stores/retrieves it from the database.

### 4. **Database Layer**
This layer represents the actual database and is responsible for:

- **Database Operations:** Performs **CRUD (Create, Read, Update, Delete)** operations on the database.

---

## **Software Structure**

The project is divided into multiple modules, including the **Order Service**, **Email Service**, **Stock Service**, and **Base Domain** that shares common logic across services. The services communicate through **Apache Kafka**.

![Architecture Diagram](image_link)  
*Above: Example architecture diagram for reference.*

---

## **Getting Started**

Follow the steps below to set up and run the application locally.

### Step 1: Clone the Repository

Clone the repository to your local machine:

```bash
git clone https://github.com/your-username/kafka-microservices.git
cd kafka-microservices
