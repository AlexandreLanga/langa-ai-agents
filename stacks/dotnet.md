# C# & .NET Engineering Guide

## Architecture & Design Patterns
- **Clean Architecture / DDD:** Keep Core Domain isolated from UI, Infra, and DB. Use Dependency Inversion (`Microsoft.Extensions.DependencyInjection`).
- **SOLID & OOP:**
  - Prefer interfaces (`IUserRepository`) over concrete classes for testability and loose coupling.
  - Use `record` or `readonly struct` for Immutable DTOs/Value Objects (`init`-only properties).
- **Asynchronous Programming:**
  - Always use `async/await` end-to-end for I/O operations (DB, HTTP, files).
  - Pass `CancellationToken` through all async call chains. Avoid `Task.Result` or `.Wait()` (prevents deadlocks).

## Code Quality & Conventions
- **Naming Conventions:**
  - `PascalCase`: Classes, Methods, Properties, Interfaces (prefixed with `I`, e.g., `IService`).
  - `camelCase`: Local variables, parameters, `_privateFields` (prefixed with underscore).
- **Pattern Matching & LINQ:**
  - Leverage modern C# pattern matching (`switch` expressions, property patterns).
  - Use LINQ for readability, but avoid complex multi-line LINQ in hot paths (prefer `foreach` for performance-critical loops).
- **Error Handling:**
  - Do not use exceptions for flow control. Use Result patterns (`Result<T>`) or domain-specific exceptions.
  - Use structured logging (`ILogger<T>`) with semantic message templates (`"User {UserId} logged in"`).

## Testing & Safety
- **Frameworks:** xUnit / NUnit + FluentAssertions + Moq / NSubstitute.
- **Safety:** Enable Nullable Reference Types (`<Nullable>enable</Nullable>`) in `.csproj`. Avoid `!` (null-forgiving operator) unless strictly guaranteed.