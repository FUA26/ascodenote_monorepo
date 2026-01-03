# ascodenote_monorepo

**Enterprise Level Boilerplate**

This is an enterprise-level monorepo boilerplate designed for scalability and maintainability. It utilizes [Turborepo](https://turborepo.com/) for high-performance build system management and [pnpm](https://pnpm.io/) for efficient package management.

## What's inside?

This repository includes the following applications and shared packages:

### Applications

- **express**: An [Express](https://expressjs.com/) backend server.
- **nestjs**: A [NestJS](https://nestjs.com/) backend application.
- **nextjs**: A [Next.js](https://nextjs.org/) frontend application (Storefront).
- **vite**: A [Vite](https://vitejs.dev/) Single Page Application (Admin Dashboard).
- **remix**: A [Remix](https://remix.run/) application (Blog).

### Shared Packages

- `@repo/ui`: A shared React UI library.
- `@repo/logger`: Isomorphic logger utility.
- `@repo/eslint-config`: Shared ESLint configurations.
- `@repo/jest-presets`: Shared Jest configurations.
- `@repo/typescript-config`: Shared TypeScript configurations.

## Getting Started

To get started with development:

1.  **Install dependencies:**

    ```sh
    pnpm install
    ```

2.  **Run development server:**
    ```sh
    pnpm run dev
    ```

For detailed development workflows (commits, versioning, quality checks), please refer to [docs/development.md](docs/development.md).

## Utilities

- [TypeScript](https://www.typescriptlang.org/) for static type checking.
- [ESLint](https://eslint.org/) for code linting.
- [Jest](https://jestjs.io) for testing.
- [Prettier](https://prettier.io) for code formatting.
