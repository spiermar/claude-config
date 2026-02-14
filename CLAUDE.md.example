# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

[Provide a brief description of what the project does]
- Main objetive and use cases
- The main outcomes (what “success” means)
- Primary users or consumers (humans, internal services, external customers)

## Tech Stack

[Describe the tech stack being used in this project]
- Language(s) and version constraints: <...>
- Frameworks: <...>
- Tooling: <package manager, build, CI>
- Data: <DB/queue/cache>

## Development Commands

```bash
# Install dependencies
npm install

# Build the project
npm run build

# Run in development mode with hot reload
npm run dev

# Run production build
npm run start
```

## Testing

```bash
# Run all tests
npm test

# Run tests in watch mode
npm run test:watch

# Run a single test file
npm test path/to/test-file.test.ts

# Run tests with coverage
npm run test:coverage
```

## Code Quality

```bash
# Lint code
npm run lint

# Fix linting issues
npm run lint:fix

# Type check
npm run typecheck

# Format code
npm run format
```

## Coding Standards and Conventions

### Style & Tooling
- Formatter: <Prettier/Black/...> (run via `<command>`)
- Lint: <ESLint/Ruff/...> (run via `<command>`)
- Types: <rules like "no any", "strict true", etc.>

### Conventions
- Naming: <files, folders, components, functions>
- Imports: <absolute vs relative, alias rules>
- Errors: <how to throw/return errors>
- Logging: <logger to use, what not to log>

### Preferred Patterns (Copy These)
- New API endpoint: see `<path/to/example>`
- New DB model + migration: see `<path/to/example>`
- New UI feature: see `<path/to/example>`

### Testing Requirements
- New business logic: <unit/integration expectations>
- Frameworks: <jest/pytest/...>
- Mocking policy: <...>

### Guardrails
- No new deps without approval.
- Don’t break public contracts (API/events).
- Security: never log secrets/PII; use existing validators.

### Git Branching Rules
- Use semantic naming: `type/description` (e.g., `feature/login-page`, `fix/header-bug`)
- Types: `feat/`, `fix/`, `chore/`, `docs/`, `refactor/`
- Include ticket numbers when applicable: `feat/JIRA-123-description`
- Use lowercase and hyphens for separators
- Always create a new branch for new tasks using `/branch`

### Version Control
- Use Conventional Commits specification for git commit messages
- Use semantic versioning (SemVer)

## Model Context Protocol (MCP) Servers

## Architecture

[Describe the main architectural pattern - e.g., "This is a monorepo using Turborepo with multiple packages" or "This follows a clean architecture with distinct layers"]
- <Component A>: <responsibility>
- <Component B>: <responsibility>
- Key flows: <request -> processing -> storage -> response>

### Project Structure

- `src/` - [Brief description of main source organization]
- `tests/` - [Testing strategy and organization]
- `packages/` - [If monorepo, describe package relationships]

### Data Flow

[Describe how data flows through the application - e.g., "API requests flow through middleware → controllers → services → repositories" or "State management uses Redux with thunks for async operations"]

### Important Patterns

[List critical architectural decisions or patterns that aren't obvious from individual files - e.g., "All database queries use the Repository pattern defined in src/db/repositories/", "Feature flags are controlled through src/config/features.ts"]

## Configuration

[Describe environment setup and configuration files]
- Environment variables are loaded from `.env` files
- [Key configuration locations and what they control]

## Database

```bash
# Run migrations
npm run db:migrate

# Rollback migration
npm run db:rollback

# Seed database
npm run db:seed
```

## Workflows

[Describe the different workflows that are part of the development process]
- Deployment process (staging, production)
- Submitting a PR
- Fixing an issue
- Handling issues and todo lists
- Adding a features (new API endpoint, etc)

## Constraints / Guardrails
- <Must / must-not rules, security, compatibility, performance>

## Important Context

[Include any non-obvious gotchas or important context]
- [e.g., "The authentication system uses JWT tokens stored in httpOnly cookies"]
- [e.g., "Background jobs are processed using Bull queues; redis must be running"]
- [e.g., "API versioning is handled via URL path (/api/v1, /api/v2)"]

### Terminology

[Describe project specific terminology]

- **Member**: A user’s membership in an org/project with a role (not the same as “User”).
- **Role**: Permission bundle assigned to a member (e.g., admin/editor/viewer).
- **Job**: An async background task executed by workers (retriable, idempotent).
- **Event**: A typed record of something that happened (used for audit/integrations).

### External Resources

- Links to documentation
- API references
- Design documents or specs
- Related repositories