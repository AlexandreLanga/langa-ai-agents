# C# / .NET

- Detect SDK and target framework from global.json, project files and pipelines; do not upgrade without need.
- Preserve nullable, async/await, DI and error-handling conventions. Add layers only when complexity warrants them.
- Use the existing test framework (xUnit/NUnit/MSTest); use doubles for external dependencies when useful.
- For behavior changes, test first, confirm failure, implement minimally, then refactor.
