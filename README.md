# Health Risk Dashboard Monorepo

## Overview
Health Risk Dashboard is a monorepo that combines a Spring Boot backend and a React + TypeScript frontend to deliver health analytics features in a single deployable stack. The repository is designed to keep shared conventions, tooling, and automation in one place so both applications can evolve together.

## Tech stack
- **Backend:** Java 21, Spring Boot, Gradle Wrapper.
- **Frontend:** React, TypeScript, Vite, PNPM.
- **Common tooling:** EditorConfig, Conventional Commits, GitHub Actions (planned).

## Repository structure
```
/                        # Monorepo root with shared tooling and docs
├─ backend/              # Spring Boot application (Java 21)
└─ frontend/             # React + TypeScript + Vite single-page app
```

## Prerequisites
- Java Development Kit (JDK) 21
- Node.js 18+ (Corepack recommended)
- PNPM 8+ (`corepack enable` to manage automatically)
- Docker (optional) for local infrastructure dependencies

## Getting started
1. Clone the repository and install toolchain prerequisites.
2. Enable the PNPM package manager:
   ```bash
   corepack enable
   ```
3. Install frontend dependencies and start the dev server:
   ```bash
   cd frontend
   pnpm install
   pnpm dev
   ```
4. Build and run the backend service:
   ```bash
   cd backend
   ./gradlew bootRun
   ```

## Testing
- **Backend:** `./gradlew test`
- **Frontend:** `pnpm test`

## Continuous integration
Automated workflows should validate formatting, linting, tests, and build steps for both applications. Add shared CI configurations in the repository root (e.g., `.github/workflows/`).

## Contributing
Refer to [CONTRIBUTING.md](CONTRIBUTING.md) for commit conventions, branch naming, and the review checklist.
