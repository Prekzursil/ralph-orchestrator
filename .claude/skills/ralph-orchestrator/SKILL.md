```markdown
# ralph-orchestrator Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `ralph-orchestrator` TypeScript codebase. You'll learn how to structure files, write imports/exports, follow commit message conventions, and understand the project's testing patterns. This guide is ideal for contributors aiming for consistency and maintainability in this repository.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names.
  - Example: `myModule.ts`, `userService.ts`

### Import Style
- Use **relative imports** for referencing local modules.
  - Example:
    ```typescript
    import { fetchData } from './apiClient';
    import { processUser } from '../utils/userUtils';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // In userService.ts
    export function getUser(id: string) { ... }
    export const USER_ROLE = 'admin';
    ```

### Commit Messages
- Follow the **Conventional Commits** specification.
- Use the `chore` prefix for maintenance and non-functional changes.
- Keep commit messages concise (average ~76 characters).
  - Example:
    ```
    chore: update dependencies to latest versions
    ```

## Workflows

### Code Contribution
**Trigger:** When adding new features or fixing bugs  
**Command:** `/contribute`

1. Create a new branch from `main`.
2. Write code using camelCase file names and relative imports.
3. Use named exports for all modules.
4. Write or update relevant tests (see Testing Patterns).
5. Commit changes using the conventional commit format.
6. Open a pull request for review.

### Dependency Maintenance
**Trigger:** When updating or adding dependencies  
**Command:** `/update-deps`

1. Update dependencies in `package.json`.
2. Run tests to ensure compatibility.
3. Commit with a message like `chore: update dependencies`.
4. Push changes and open a pull request.

## Testing Patterns

- Test files use the pattern `*.test.*` (e.g., `userService.test.ts`).
- The testing framework is not specified; check existing test files for structure.
- Place tests alongside the modules they test or in a dedicated `__tests__` directory.
- Example test file:
  ```typescript
  // userService.test.ts
  import { getUser } from './userService';

  describe('getUser', () => {
    it('returns user data for valid id', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command        | Purpose                                 |
|----------------|-----------------------------------------|
| /contribute    | Start a new feature or bugfix workflow  |
| /update-deps   | Update project dependencies             |
```
