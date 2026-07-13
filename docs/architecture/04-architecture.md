# Gardenia Architecture

## Purpose

This document describes the architectural decisions made during the development of the Gardenia platform.

The objective is to build a maintainable, testable, scalable, and business-oriented application.

---

# Why Clean Architecture?

Gardenia is intended to be both:

- A real business application.
- A professional learning project.

For this reason, Clean Architecture has been selected instead of a traditional layered architecture.

The goal is to keep business rules independent from frameworks, databases, and UI technologies.

---

# Architectural Principles

The project follows these principles.

- Separation of concerns.
- Single Responsibility Principle.
- Dependency Inversion Principle.
- Business logic independent of infrastructure.
- Framework independence.
- Testability.
- Maintainability.

---

# Solution Structure

Gardenia.Api

Responsible for:

- HTTP Endpoints
- Authentication
- Dependency Injection configuration
- API documentation
- Request/Response handling

The API should contain as little business logic as possible.

---

Gardenia.Application

Responsible for:

- Use Cases
- DTOs
- Interfaces
- Application services
- Validation
- Business workflows

This layer coordinates the business operations.

---

Gardenia.Domain

Responsible for:

- Entities
- Value Objects (future)
- Domain Services (future)
- Business Rules
- Domain Exceptions

This is the heart of the application.

The Domain layer must not depend on any external framework.

---

Gardenia.Infrastructure

Responsible for:

- Entity Framework Core
- SQL Server
- Repository implementations
- External services
- File Storage
- Payment providers (future)

Infrastructure implements the contracts defined by the Application layer.

---

# Dependency Rule

Dependencies always point inward.

Api

↓

Application

↓

Domain

Infrastructure

↓

Application

↓

Domain

The Domain project should never reference any other project.

---

# Technologies

Backend

- ASP.NET Core
- Entity Framework Core
- SQL Server

Frontend

- Angular
- TypeScript

Development

- Visual Studio 2026
- Visual Studio Code
- Git
- GitHub

Future

- Docker
- Azure
- GitHub Actions

---

# Architectural Decisions

Decision 001

Use Clean Architecture.

Reason:

Business rules should remain independent from infrastructure.

---

Decision 002

Use Repository Pattern.

Reason:

Application logic should not know how data is persisted.

---

Decision 003

Use Entity Framework Core.

Reason:

Provides modern ORM capabilities while maintaining productivity.

---

Decision 004

Use SQL Server.

Reason:

Primary relational database for the project.

---

Decision 005

Backend and Frontend will be maintained in separate repositories.

Reason:

Improves portfolio organization and reflects common industry practices.

---

# Future Evolution

The architecture may evolve over time.

Future improvements may include:

- CQRS
- MediatR (evaluation required)
- Domain Events
- Event-Driven integrations
- Docker
- Azure
- CI/CD