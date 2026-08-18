<div align="center">

# 💼 Human Resources Management Backend

**A Spring Boot REST backend for job seekers, employers, job listings, workforce reference data, verification, and image management.**

![Java](https://img.shields.io/badge/Java-11-E76F00?style=for-the-badge&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-REST_API-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-API_Docs-85EA2D?style=for-the-badge&logo=swagger&logoColor=111827)
![Cloudinary](https://img.shields.io/badge/Cloudinary-Images-3448C5?style=for-the-badge&logo=cloudinary&logoColor=white)

</div>

---

## ✨ Overview

This repository contains an HR management backend built around recruitment workflows. It supports job seekers, employers, job listings, job positions, workplaces, work times, cities, approval workflows, and image uploads through a layered Spring Boot application.

The application source is located inside `HRMS_Backend-master`.

## 🚀 Features

- Job-seeker and employer registration and lookup.
- Job creation, visibility changes, approval queries, and date-based filtering.
- Job-position, city, workplace, and work-time reference endpoints.
- Account activation and approval operations.
- External identity-check adapter integration.
- Email-verification abstraction.
- Cloudinary-backed image upload adapter.
- Consistent result and data-result response objects.
- PostgreSQL persistence through Spring Data JPA.
- Swagger-based API documentation support.

## 🧱 Architecture

```text
API Controllers
      │
      ▼
Business Services & Managers
      │
      ├──► Verification / Email / Image Adapters
      ▼
Spring Data DAOs
      │
      ▼
PostgreSQL
```

```text
HRMS_Backend-master/
├── src/main/java/kodlama/io/hrms/
│   ├── api/controllers/
│   ├── business/
│   ├── core/utilities/
│   ├── dataAccess/
│   └── entities/
├── APIDocumentation.md
├── PostgreDatabaseSQL
└── pom.xml
```

## 🔌 API Areas

| Base path | Responsibility |
|---|---|
| `/api/jobseekers/` | Job-seeker operations |
| `/api/employers/` | Employer operations |
| `/api/jobs/` | Job listing and visibility workflows |
| `/api/jobpositions/` | Job-position reference data |
| `/api/cities/` | City management |
| `/api/workplaces/` | Workplace reference data |
| `/api/worktimes/` | Work-time reference data |
| `/api/activationpanel/` | Approval and activation workflows |
| `/api/images/` | Image upload |

See [`HRMS_Backend-master/APIDocumentation.md`](HRMS_Backend-master/APIDocumentation.md) for the repository's detailed API notes.

## ⚙️ Getting Started

### Prerequisites

- JDK 11
- Maven
- PostgreSQL

### Configure

Set local PostgreSQL values in `HRMS_Backend-master/src/main/resources/application.properties`:

```properties
spring.datasource.url=<your-jdbc-url>
spring.datasource.username=<your-username>
spring.datasource.password=<your-password>
```

Review `HRMS_Backend-master/PostgreDatabaseSQL` for the database setup material. Keep all real credentials outside Git.

### Run

```bash
git clone https://github.com/AhmedRmadanMohamed/Human-Resources.git
cd Human-Resources/HRMS_Backend-master
mvn spring-boot:run
```

### Test

```bash
mvn test
```

## 📝 Repository Note

The committed `target` directory contains generated build output. The canonical source is under `src`; generated artifacts should be recreated by Maven rather than maintained manually.

## 🗺️ Roadmap

- Externalize secrets and third-party service configuration.
- Remove generated build and IDE files from version control.
- Expand service and controller tests.
- Upgrade the API documentation stack.
- Add authentication and authorization for administrative endpoints.

---

<div align="center">

A layered Java backend for practical recruitment and HR workflows.

</div>
