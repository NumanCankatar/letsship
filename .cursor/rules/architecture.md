# Cursor Architecture Rules for ShipFast Project

## 1. Directory Structure
- Maintain the following top-level directories:
  - `app/` for all Next.js pages, API routes, and route handlers.
  - `components/` for reusable React components.
  - `libs/` for utility functions, API clients, and hooks.
  - `public/` for static assets.
- Do not create new top-level directories unless absolutely necessary.

## 2. Component Conventions
- All React components must be placed in `components/` or a relevant subdirectory of `app/` if they are page-specific.
- Component filenames and exported function names must start with an uppercase letter (e.g., `UserSurvey.js`, `OptionComponent.js`).
- Use functional components and React hooks. Do not use class components.
- Keep components focused and reusable. Extract logic into hooks in `libs/` if shared.

## 3. API Route Conventions
- All API routes must be placed under `app/api/`.
- Use RESTful naming conventions for API endpoints (e.g., `/api/user/createSurvey`).
- Each API route should be in its own file or directory, following Next.js conventions.
- Use async/await for all asynchronous operations.
- Handle errors gracefully and return appropriate HTTP status codes.

## 4. Utility and Library Code
- Place all shared logic, hooks, and API clients in `libs/`.
- Do not duplicate logic between components and API routes; extract to `libs/` if reused.

## 5. Styling
- Use Tailwind CSS for all styling.
- Do not use inline styles except for dynamic or one-off cases.
- Place global styles in `app/globals.css`.

## 6. Naming and Exports
- Use PascalCase for component and file names.
- Use camelCase for variables and functions.
- Default export for components, named export for utilities/hooks.

## 7. Environment and Configuration
- Store all environment variables in `.env.local` and document them in the README.
- Do not hardcode secrets or API keys in the codebase.

## 8. Documentation
- Update the README with any architectural or structural changes.
- Document new components, utilities, and API endpoints with usage examples.

## 9. Testing and Linting
- Ensure all code passes ESLint checks (see `.eslintrc.json`).
- Write tests for critical logic if possible (add a `__tests__` directory if needed).

---

**Purpose:**
These rules ensure the project remains maintainable, scalable, and consistent as it grows. All contributors should follow these guidelines for any new code or refactoring. 