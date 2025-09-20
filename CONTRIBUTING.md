# Contributing

Thank you for helping improve the Health Risk Dashboard! This guide covers how we work together across the backend and frontend projects.

## Development workflow
1. Discuss significant changes via an issue or architecture note before writing code.
2. Fork the repo (if external) and create a dedicated branch from `main` (see branching model below).
3. Keep changes focused: separate backend, frontend, and infrastructure updates into logical commits.
4. Ensure all automated checks pass locally before requesting a review.

## Commit style
We follow [Conventional Commits](https://www.conventionalcommits.org/) to keep a clean history and automate changelog generation.

- Use the format `<type>(optional scope): <summary>` (e.g., `feat(frontend): add risk trends chart`).
- Keep summaries under 72 characters and use the imperative mood.
- Include body and footer details when they add context (e.g., breaking changes, issue references).

Common commit types: `feat`, `fix`, `chore`, `docs`, `refactor`, `test`, `build`, `ci`.

## Branching model
- `main` is always releasable; it holds production-ready code.
- Create short-lived branches off `main` using a descriptive prefix:
  - `feature/<summary>` for new features
  - `bugfix/<summary>` for fixes
  - `chore/<summary>` for maintenance tasks
- Rebase your branch onto the latest `main` before opening a pull request.
- Delete feature branches after merging to keep the repository tidy.

## Pull request checklist
Before requesting review:
- [ ] Ensure commits follow the Conventional Commits standard.
- [ ] Update documentation, changelog entries, or configuration files touched by the change.
- [ ] Add or update automated tests and confirm they pass (`./gradlew test`, `pnpm test`).
- [ ] Run linters/formatters as applicable (e.g., `./gradlew check`, `pnpm lint`, `pnpm format`).
- [ ] Verify build artifacts: `./gradlew bootJar` for backend, `pnpm build` for frontend.
- [ ] Confirm no secrets or sensitive data are present in the code or configuration.
- [ ] Request reviewers who own the affected area and provide context for manual testing when needed.

## Code review expectations
- Authors respond promptly to feedback and keep discussions respectful.
- Reviewers focus on correctness, maintainability, security, and developer experience.
- Small follow-up issues can be tracked with TODOs or separate tasks; blocking items must be addressed before merge.
- Use squash merge for PRs to maintain a linear history (the squash commit must still follow Conventional Commit format).

## Releasing
- Tag releases from `main` (e.g., `v1.2.0`) after CI passes.
- Document release notes summarizing key backend and frontend changes.

Happy building!
