# Project Overview

## Introduction

The `ascodenote_monorepo` is a comprehensive monorepo setup based on the [Turborepo](https://turborepo.com/) kitchen sink starter. It is designed to demonstrate a scalable architecture for modern web applications, facilitating the development of multiple applications and shared packages within a single repository.

## Technology Stack

- **Monorepo Management**: [Turborepo](https://turborepo.com/)
- **Package Manager**: [pnpm](https://pnpm.io/)
- **Languages**: 100% [TypeScript](https://www.typescriptlang.org/) for type safety.
- **Linting & Formatting**: [ESLint](https://eslint.org/) and [Prettier](https://prettier.io/).
- **Testing**: [Jest](https://jestjs.io/).

## Core Components

The repository is divided into applications (`apps/`) and shared packages (`packages/`).

### Applications

- **express**: An Express.js backend server.
- **nestjs**: A NestJS backend application.
- **nextjs**: A Next.js frontend application for the customer-facing store.
- **vite**: A Vite-based Single Page Application (SPA) for the administration dashboard.
- **remix**: A Remix application for content publishing.

### Shared Packages

- **@repo/ui**: A shared React UI component library (e.g., `<CounterButton>`, `<Link>`).
- **@repo/logger**: A consistent logging utility.
- **@repo/eslint-config**: Shared ESLint configurations to enforce code quality.
- **@repo/jest-presets**: Shared Jest configurations for testing.
- **@repo/typescript-config**: Shared TypeScript configurations (`tsconfig.json`).

## Getting Started

To get started with the project, install dependencies and run the development server:

```bash
pnpm install
pnpm run dev
```

This will start all applications in development mode using Turborepo's parallel execution capabilities.
