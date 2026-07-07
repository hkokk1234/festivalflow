# FestivalFlow

FestivalFlow is a production-style Spring Boot application for managing music festivals end to end. It combines role-based access control, festival operations, performance management, and a polished web UI into one cohesive system that feels far more like a real product than a classroom demo.

## Why this project stands out

This project is designed to show strong backend architecture and thoughtful product thinking:

- Role-based access across Admin, Organizer, Staff, Artist, and User roles
- Festival and performance lifecycle management
- Operational details such as technical requirements, merchandise, rehearsal slots, and setlists
- A responsive web interface for navigation and day-to-day workflows
- Automated tests and a clean, maintainable Spring Boot structure

## Tech stack

- Java 17
- Spring Boot 3.2
- Spring Security + JWT
- Spring Data JPA
- H2 in-memory database
- Maven
- Responsive server-rendered UI

## Project structure

- Backend services and controllers live under src/main/java
- Entity and repository layers model the domain clearly and independently
- Static assets and UI pages live under src/main/resources/static
- Test coverage is included under src/test/java

## Running locally

The application uses an embedded H2 database, so no external database setup is required.

```bash
./mvnw spring-boot:run
```

Then open:

- http://localhost:8080/
- http://localhost:8080/h2-console

## Portfolio notes

This project was intentionally structured to look professional and interview-ready:

- Clear domain boundaries and layered architecture
- Strong error handling and readable configuration
- Clean documentation and a polished first-run experience
- Good candidate for demonstrating backend engineering, security, and product-oriented thinking

## Next improvements

- Add end-to-end API tests for permission boundaries
- Introduce payment and ticketing workflows
- Add email notifications and admin analytics
