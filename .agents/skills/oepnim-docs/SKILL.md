```markdown
# oepnim-docs Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill covers the core development patterns and conventions used in the `oepnim-docs` repository, a TypeScript-based project with no detected framework. It details file naming, import/export styles, commit message conventions, and testing patterns to help maintain consistency and quality in contributions.

## Coding Conventions

### File Naming
- Use **kebab-case** for all file names.
  - Example:  
    ```
    user-profile.ts
    api-client.test.ts
    ```

### Import Style
- Use **relative imports** for referencing modules within the project.
  - Example:
    ```typescript
    import { fetchData } from './utils/fetch-data';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // In utils/format-date.ts
    export function formatDate(date: Date): string {
      // implementation
    }
    ```

### Commit Message Convention
- Follow the **Conventional Commits** standard.
- Use the `feat` prefix for new features.
- Keep commit messages concise (average ~57 characters).
  - Example:
    ```
    feat: add user authentication module
    ```

## Workflows

### Feature Development
**Trigger:** When adding a new feature  
**Command:** `/feature`

1. Create a new branch using kebab-case for the feature name (e.g., `feature/add-user-auth`).
2. Implement the feature using TypeScript, following file naming and import/export conventions.
3. Write or update corresponding test files (`*.test.ts`).
4. Commit changes using the `feat` prefix and a concise description.
5. Open a pull request for review.

### Testing
**Trigger:** When verifying code changes  
**Command:** `/test`

1. Identify or create test files matching the pattern `*.test.ts`.
2. Run the test suite using the project's test runner (framework unknown; refer to project scripts).
3. Ensure all tests pass before merging or submitting a pull request.

### Code Review
**Trigger:** Before merging changes  
**Command:** `/review`

1. Ensure code follows all documented conventions.
2. Verify commit messages use the correct format.
3. Confirm all tests pass.
4. Review code for clarity and maintainability.

## Testing Patterns

- Test files use the `*.test.ts` naming pattern.
- The specific testing framework is not detected; check project documentation or scripts for details.
- Place tests alongside the modules they cover or in a dedicated test directory.
- Example test file:
  ```typescript
  // utils/format-date.test.ts
  import { formatDate } from './format-date';

  describe('formatDate', () => {
    it('formats date as YYYY-MM-DD', () => {
      expect(formatDate(new Date('2024-01-01'))).toBe('2024-01-01');
    });
  });
  ```

## Commands
| Command    | Purpose                                  |
|------------|------------------------------------------|
| /feature   | Start a new feature development workflow  |
| /test      | Run the test suite                       |
| /review    | Begin code review process                |
```