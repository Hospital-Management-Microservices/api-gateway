# API Gateway
## Hospital Management System - Microservices Assignment
### IT4020 - Modern Topics in IT | SLIIT 2026

---

## Port: 8080

---

## Tech Stack
- Java 17
- Spring Boot 3.2.0
- Spring Cloud Gateway 2023.0.0
- Maven

---

## Setup Instructions

### Step 1 - Clone the repository
```bash
git clone https://github.com/YOUR_ORG/api-gateway.git
cd api-gateway
```

### Step 2 - Make sure ALL services are running first!
```
Patient Service      → localhost:8081  ✅
Doctor Service       → localhost:8082  ✅
Appointment Service  → localhost:8083  ✅
Department Service   → localhost:8084  ✅
Medical Record       → localhost:8085  ✅
```

### Step 3 - Run the gateway
```bash
mvn spring-boot:run
```

---

## API Routes

### Service Routes
| Gateway URL | Routes To | Port |
|-------------|-----------|------|
| localhost:8080/patients/** | Patient Service | 8081 |
| localhost:8080/doctors/** | Doctor Service | 8082 |
| localhost:8080/appointments/** | Appointment Service | 8083 |
| localhost:8080/departments/** | Department Service | 8084 |
| localhost:8080/medical-records/** | Medical Record Service | 8085 |

---

## Swagger URLs Via Gateway

| Service | Direct Swagger | Via Gateway |
|---------|---------------|-------------|
| Patient | localhost:8081/swagger-ui.html | localhost:8080/patients/swagger-ui.html |
| Doctor | localhost:8082/swagger-ui.html | localhost:8080/doctors/swagger-ui.html |
| Appointment | localhost:8083/swagger-ui.html | localhost:8080/appointments/swagger-ui.html |
| Department | localhost:8084/swagger-ui.html | localhost:8080/departments/swagger-ui.html |
| Medical Record | localhost:8085/swagger-ui.html | localhost:8080/medical-records/swagger-ui.html |

---

## Test Gateway is Running
```
http://localhost:8080/actuator/health
```
Should return: {"status":"UP"}
