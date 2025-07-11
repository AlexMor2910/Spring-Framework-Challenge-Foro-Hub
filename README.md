# ForoHub Java API

This is a Spring Boot project for managing discussion topics in a forum-style application. It includes basic CRUD functionality using a relational database and follows good practices such as validation, clean architecture, and separation of concerns.

## Features

- Create a new topic (`POST /topicos`)
- List all topics (`GET /topicos`)
- View topic details by ID (`GET /topicos/{id}`)
- Update a topic (`PUT /topicos/{id}`)
- Delete a topic (`DELETE /topicos/{id}`)
- Optional: Pagination and sorting on topic list

## Technology Stack

- Java 17+
- Spring Boot
- Spring Web
- Spring Data JPA
- H2 in-memory database (for development/testing)
- Bean Validation (Jakarta Validation API)

## Getting Started

### Prerequisites

- Java JDK 17 or newer
- Maven or Gradle (optional if using IDE)

### Running the Application

1. Clone the repository or unzip the provided folder.
2. Navigate into the project directory.
3. Run the application using your IDE or:

```bash
./mvnw spring-boot:run
```

or

```bash
./gradlew bootRun
```

4. Access the H2 database console (optional for debugging) at:

```
http://localhost:8080/h2-console
```

JDBC URL: `jdbc:h2:mem:foro`

### Example Request

#### POST /topicos

```json
{
  "titulo": "¿Cómo funciona Spring Boot?",
  "mensaje": "Estoy aprendiendo sobre controladores.",
  "autor": "Juan Pérez",
  "curso": "Java Spring"
}
```

## Notes

- All fields are required.
- Duplicate topics (same title and message) are not allowed.
- Pagination and sorting are implemented in `GET /topicos`.

## License

This project is provided as part of a learning challenge. Use it freely for educational purposes.
