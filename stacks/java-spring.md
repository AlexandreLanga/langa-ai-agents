# Java & Spring Boot Engineering Guide

## Architecture & Design Patterns
- **Hexagonal / Layered Architecture:** Separate `Controller` (REST), `Service` (Business), `Repository` (Data), and `Domain` (Core logic).
- **Spring Standards:**
  - Use **Constructor Injection** over `@Autowired` field injection (promotes immutability and testability).
  - Use `@Transactional` deliberately on service layer methods (specify `readOnly = true` for queries).
- **OOP & Immutability:**
  - Use Java **Records** for DTOs and immutable data carriers.
  - Keep domain entities rich in business behavior (avoid anemic domain models).

## Code Quality & Conventions
- **Naming Conventions:**
  - `PascalCase`: Classes, Interfaces, Enums.
  - `camelCase`: Variables, Methods, Fields.
  - `UPPER_SNAKE_CASE`: Constants (`static final`).
- **Functional Programming & Streams:**
  - Use `Stream` API for declarative collection transformations; avoid side effects inside `map`/`filter`.
  - Use `Optional<T>` as a return type for methods that might not return a value. Never pass `Optional` as a parameter or store it as a field.
- **Error Handling:**
  - Handle exceptions globally using `@ControllerAdvice` and `@ExceptionHandler`.
  - Prefer custom Runtime Exceptions for domain errors over checked exceptions.

## Testing & Safety
- **Frameworks:** JUnit 5 + AssertJ + Mockito. Use `@WebMvcTest` for controller slices and `@DataJpaTest` for persistence testing.
- **Safety:** Prevent SQL Injection via Spring Data JPA / Parameterized Queries. Never expose raw Entities through REST APIs (map to DTOs using MapStruct or custom mappers).