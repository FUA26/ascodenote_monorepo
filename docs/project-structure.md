# Project Structure

This document provides a detailed breakdown of the `ascodenote_monorepo` folder structure and the purpose of each directory.

## Root Directory

- **`apps/`**: Contains the source code for the individual applications.
- **`packages/`**: Contains shared libraries and configuration packages used by the apps.
- **`docs/`**: Project documentation and Product Requirement Documents (PRDs).
- **`package.json`**: Root configuration defining workspaces and global scripts.
- **`turbo.json`**: Configuration for Turborepo's build pipeline and task dependencies.

## Apps Directory (`apps/`)

Each folder inside `apps` represents a deployable application:

| App       | Framework    | Purpose                                    |
| :-------- | :----------- | :----------------------------------------- |
| `express` | Express.js   | Backend API server.                        |
| `nestjs`  | NestJS       | Backend server (NestJS).                   |
| `nextjs`  | Next.js      | E-commerce / Frontend website.             |
| `vite`    | Vite (React) | Admin dashboard for managing the platform. |
| `remix`   | Remix        | Blog platform.                             |

## Packages Directory (`packages/`)

Shared code and configurations to reduce duplication and ensure consistency:

| Package             | Purpose                                                                       |
| :------------------ | :---------------------------------------------------------------------------- |
| `ui`                | Component library containing shared React components (buttons, inputs, etc.). |
| `logger`            | Utility for consistent logging across apps.                                   |
| `eslint-config`     | ESLint rules shared across the entire monorepo.                               |
| `jest-presets`      | Jest configuration presets for testing.                                       |
| `typescript-config` | Base `tsconfig.json` files extended by other packages/apps.                   |

## Key Configuration Files

- **`pnpm-workspace.yaml`**: Defines the workspace topology for pnpm.
