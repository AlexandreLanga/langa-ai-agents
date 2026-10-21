# Python Engineering Guide

## Architecture & Design Patterns
- **Modularity & OOP:**
  - Organize code into cohesive packages with clear public APIs via `__all__` or explicit exports.
  - Use `dataclasses` or `Pydantic` models for structured data and payload validation.
  - Prefer Composition over Inheritance for extending functionality.
- **Framework Standards:**
  - **FastAPI / Flask:** Use dependency injection for DB sessions and services. Keep routes thin and delegate logic to domain services.
  - **Django:** Keep business logic in domain models/services, not in Views or Serializers ("Fat Models / Thin Views").

## Code Quality & Conventions (PEP 8 & Clean Code)
- **Typing:** Use type hints everywhere (`def process_order(order_id: str) -> Order:`). Run `mypy` or `pyright` in strict mode.
- **Naming Conventions:**
  - `snake_case`: Variables, Functions, Methods, Modules, Packages.
  - `PascalCase`: Classes, Exceptions.
  - `UPPER_SNAKE_CASE`: Constants.
- **Pythonic Idioms:**
  - Use List/Dict comprehensions judiciously; avoid deeply nested comprehensions.
  - Use Context Managers (`with` statements) for resource management (files, locks, DB transactions).
  - Use explicit exception handling (`except SpecificError:` instead of bare `except:`).

## Testing & Safety
- **Frameworks:** `pytest` + `pytest-asyncio` + `unittest.mock`.
- **Environment & Safety:** Enforce virtual environments (Poetry, uv, or venv). Use `black`/`ruff` for deterministic code formatting and linting.