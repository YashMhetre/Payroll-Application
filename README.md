# Payroll Application

## Overview
This Payroll Application is a full-stack web application that helps organizations manage employee payroll, track leave applications, and handle leave requests efficiently. The system is designed with microservices architecture and utilizes modern tools for scalability, security, and deployment.

## Tech Stack
- **Backend:** Java, Spring Boot, Spring Security, Kafka, PostgreSQL
- **Frontend:** Angular
- **Service Discovery:** Eureka Server, Gateway Server, Feign Client
- **Deployment:** Docker, Kubernetes
- **Notifications:** Kafka, Mailtrap

## Features
- Employee payroll management
- Leave tracking and application handling
- Service discovery using Eureka Server
- API Gateway for microservices communication
- Authentication and authorization
- Real-time notifications for leave applications
- Dockerized deployment with Kubernetes

## Setup Instructions

### Prerequisites
- Java 17+
- Node.js and Angular CLI
- PostgreSQL
- Docker & Kubernetes
- Apache Kafka & Zookeeper

### Backend Setup
1. Clone the repository:
   ```sh
   git clone https://github.com/YOUR_GITHUB/payroll-application.git
   cd payroll-application
   ```
2. Configure PostgreSQL in `application.properties`:
   ```properties
   spring.datasource.url=jdbc:postgresql://localhost:5432/payroll_db
   spring.datasource.username=your_username
   spring.datasource.password=your_password
   ```
3. Start Kafka and Zookeeper:
   ```sh
   docker-compose up -d
   ```
4. Build and run the backend:
   ```sh
   mvn clean install
   mvn spring-boot:run
   ```

### Frontend Setup
1. Navigate to the frontend directory:
   ```sh
   cd frontend
   ```
2. Install dependencies and start the Angular app:
   ```sh
   npm install
   ng serve --open
   ```

## Deployment
- **Docker Compose:**
  ```sh
  docker-compose up --build
  ```
- **Kubernetes Deployment:**
  ```sh
  kubectl apply -f k8s/
  ```

## API Endpoints
| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/payroll` | GET | Fetch all payroll records |
| `/api/payroll/{id}` | GET | Fetch payroll by ID |
| `/api/leave/apply` | POST | Apply for leave |
| `/api/leave/status` | GET | Fetch leave status |

## Contributing
Feel free to fork this repository and submit pull requests.

## License
This project is licensed under the MIT License.

## Contact
For any inquiries, reach out to **mhetreyash242@example.com**.

