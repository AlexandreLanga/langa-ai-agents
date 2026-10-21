# Angular & TypeScript Engineering Guide

## Architecture & State Management
- **Standalone Architecture:** Prefer Standalone Components, Directives, and Pipes (Angular 14+ / 17+ best practice).
- **Signals & Reactive Programming:**
  - Use **Angular Signals** (`signal()`, `computed()`, `effect()`) for local reactive state and fine-grained change detection.
  - Use **RxJS** for asynchronous streams, HTTP requests, and event handling.
- **Component Pattern:**
  - Maintain a strict Smart (Container) vs. Dumb (Presentational) component hierarchy.
  - Set `changeDetection: ChangeDetectionStrategy.OnPush` on presentational components.

## Code Quality & Conventions
- **TypeScript Strictness:**
  - Enforce `strict: true` in `tsconfig.json`. Avoid `any`; use `unknown` for dynamic values that require runtime narrowing.
  - Define explicit interface models for all HTTP responses and component inputs.
- **RxJS Best Practices:**
  - Always unsubscribe or use `takeUntilDestroyed()`, `async` pipe, or `first()` to avoid memory leaks.
  - Avoid nested `.subscribe()` calls; use flattening operators (`switchMap`, `concatMap`, `exhaustMap`).
- **Control Flow:**
  - Use Angular's modern built-in control flow syntax (`@if`, `@for`, `@switch`) instead of `*ngIf` / `*ngFor`.

## Testing & Safety
- **Frameworks:** Jasmine/Karma or Jest + Angular Testing Library.
- **Performance & Security:** Use `track` in `@for` loops. Prevent XSS by avoiding raw innerHTML binding without `DomSanitizer`.