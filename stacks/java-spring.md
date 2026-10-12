# Java / Spring Boot

- Detect Java, Spring Boot and build versions from manifests/pipelines; do not upgrade without need.
- Follow existing Spring DI, DTO, validation, error-handling and transaction boundaries; keep business logic out of controllers.
- Use configured test tools (e.g. JUnit/Mockito); reserve full-context tests for cases that need them.
- For behavior changes, test first, confirm failure, implement minimally, then refactor.
