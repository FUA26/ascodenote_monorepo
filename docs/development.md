# Development Workflow

This project is equipped with several tools to ensure code quality, standardized commits, and automated versioning.

## Code Quality & Git Hooks

We use [Husky](https://typicode.github.io/husky/) and [lint-staged](https://github.com/lint-staged/lint-staged) to automatically verify code before it is committed.

- **Pre-commit Hook**: When you attempt to commit changes, `lint-staged` runs:
  - `prettier --write` on all staged files (JS, TS, MD, JSON).
  - `eslint --fix` on staged TypeScript files.
- **Failures**: If linting fails, the commit will be aborted. You must fix the errors and stage the changes again.

## Conventional Commits

We enforce the [Conventional Commits](https://www.conventionalcommits.org/) specification using [Commitlint](https://commitlint.js.org/).

**Format**: `<type>(<scope>): <subject>`

**Common Types**:

- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Changes that do not affect the meaning of the code (white-space, formatting, etc)
- `refactor`: A code change that neither fixes a bug nor adds a feature
- `perf`: A code change that improves performance
- `test`: Adding missing tests or correcting existing tests
- `chore`: Changes to the build process or auxiliary tools and libraries such as documentation generation

**Example**:

```bash
git commit -m "feat(ui): add new button component"
```

## Versioning & Publishing

We use [Changesets](https://github.com/changesets/changesets) to manage versioning and changelogs.

### Workflow

1.  **Make Changes**: Implement your feature or fix.
2.  **Add Changeset**: Run the following command before committing:
    ```bash
    pnpm changeset
    ```
3.  **Select Packages**: Choose which packages are affected.
4.  **Bump Type**: Select `major`, `minor`, or `patch`.
5.  **Summary**: Enter a summary of the changes.

This creates a markdown file in `.changeset/`. When the PR is merged, the CI system will detect usage of changesets to handle version bumping and publishing.
