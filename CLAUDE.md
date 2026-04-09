# CLAUDE.md

This file provides guidance for AI assistants (Claude Code and similar tools) working in this repository.

## Repository Overview

**Repository**: `civrocker84/examples`
**Status**: Freshly initialized — no source code has been committed yet.

This repository was created to house example projects or code samples. As content is added, this file should be updated to reflect the actual codebase structure, conventions, and workflows.

## Git Workflow

### Branch Naming

Feature branches follow the pattern:
```
claude/<description>-<short-hash>
```

Example: `claude/add-claude-documentation-9TuAa`

### Commit Messages

Write clear, descriptive commit messages in the imperative mood:
- Good: `Add authentication middleware`
- Good: `Fix null pointer in user lookup`
- Avoid: `Fixed stuff`, `WIP`, `misc changes`

### Push Protocol

Always push with tracking:
```bash
git push -u origin <branch-name>
```

On network failure, retry with exponential backoff: 2s → 4s → 8s → 16s (max 4 retries).

## Development Setup

> **Note**: No project-specific tooling has been configured yet. Update this section when a stack is chosen.

Typical setup steps to document here once established:
- Runtime/language version requirements
- Dependency installation command
- Environment variable configuration (`.env.example`)
- Database or service prerequisites

## Testing

> **Note**: No test framework has been configured yet. Update this section once tests are added.

Document here:
- How to run the full test suite
- How to run a single test file
- Coverage thresholds, if enforced

## Linting and Formatting

> **Note**: No linter or formatter has been configured yet. Update this section once tooling is added.

Document here:
- Linting command
- Format check / auto-fix command
- Whether formatting is enforced in CI

## Code Conventions

> **Note**: Update this section once a language and framework are chosen.

Placeholder conventions to define:
- Language and version
- File naming style (kebab-case, snake_case, PascalCase)
- Import ordering
- Error handling patterns
- Logging approach

## CI/CD

> **Note**: No CI/CD pipeline has been configured yet.

Once configured, document:
- Which CI system is used (GitHub Actions, etc.)
- What checks run on pull requests
- Deployment process and environments

## Working with AI Assistants

### DO

- Update this file whenever the project structure changes significantly
- Keep commands in this file executable and up to date
- Prefer editing existing files over creating new ones
- Read files before modifying them
- Make focused, minimal changes scoped to the task at hand

### DON'T

- Push to `main` or `master` directly — always use a feature branch
- Commit secrets, credentials, or `.env` files
- Add speculative abstractions or features not explicitly requested
- Skip the linter/formatter before committing (once configured)
- Create a pull request unless explicitly asked to do so

## Updating This File

When the codebase grows, replace the placeholder sections above with accurate information. Specifically, update:

1. **Repository Overview** — describe what the project actually does
2. **Development Setup** — exact commands to get a local environment running
3. **Testing** — exact commands and any environment requirements
4. **Linting and Formatting** — exact commands used in CI
5. **Code Conventions** — language-specific patterns and project style decisions
6. **CI/CD** — pipeline structure and deployment targets
