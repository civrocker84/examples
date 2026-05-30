# CLAUDE.md

This file provides guidance for AI assistants (Claude Code and similar tools) working in this repository.

**Last updated**: 2026-05-30

---

## Repository Overview

**Repository**: `civrocker84/examples`  
**Status**: Freshly initialized — no source code has been committed yet.

This repository was created to house example projects or code samples. As content is added, this file should be updated to reflect the actual codebase structure, conventions, and workflows.

### Current Structure

```
examples/
└── CLAUDE.md       ← this file
```

No source code, dependencies, tests, or CI/CD configuration exist yet.

---

## Git Workflow

### Branch Protection

- **Never push directly to `main` or `master`** — always work on a feature branch.
- **Never create a pull request** unless the user explicitly asks for one.

### Branch Naming

Feature branches follow the pattern:

```
claude/<description>-<short-hash>
```

Examples observed in this repo:
- `claude/add-claude-documentation-9TuAa`
- `claude/claude-md-docs-gqhvD`

### Commit Messages

Write clear, descriptive commit messages in the imperative mood:

```
# Good
Add authentication middleware
Fix null pointer in user lookup
Update CLAUDE.md with current project structure

# Avoid
Fixed stuff
WIP
misc changes
```

### Push Protocol

Always push with upstream tracking:

```bash
git push -u origin <branch-name>
```

On network failure, retry with exponential backoff:

| Attempt | Wait before retry |
|---------|------------------|
| 1st     | 2s               |
| 2nd     | 4s               |
| 3rd     | 8s               |
| 4th     | 16s              |

Maximum 4 retries. If all fail, report the error to the user.

---

## Development Setup

> **Note**: No project-specific tooling has been configured yet. Update this section when a stack is chosen.

When a stack is chosen, document here:
- Runtime/language version requirements (e.g., `node >= 20`, `python >= 3.11`)
- Dependency installation command (e.g., `npm install`, `pip install -e .`)
- Environment variable configuration (reference `.env.example`)
- Database or external service prerequisites

---

## Testing

> **Note**: No test framework has been configured yet. Update this section once tests are added.

When tests are added, document here:
- Command to run the full test suite
- Command to run a single test file
- Coverage thresholds, if enforced
- Any environment setup required before running tests

---

## Linting and Formatting

> **Note**: No linter or formatter has been configured yet. Update this section once tooling is added.

When configured, document here:
- Lint command (e.g., `npm run lint`, `ruff check .`)
- Format check / auto-fix command (e.g., `prettier --write .`, `ruff format .`)
- Whether formatting is enforced in CI (and the exact command CI uses)

---

## Code Conventions

> **Note**: Update this section once a language and framework are chosen.

When a stack is established, define:
- Language and version
- File naming style (kebab-case, snake_case, PascalCase)
- Import ordering rules
- Error handling patterns
- Logging approach

---

## CI/CD

> **Note**: No CI/CD pipeline has been configured yet.

When CI/CD is introduced, document:
- Which system is used (GitHub Actions, CircleCI, etc.)
- What checks run on pull requests (lint, test, type-check, build)
- Deployment process and target environments

---

## Working with AI Assistants

### DO

- Read files before modifying them
- Make focused, minimal changes scoped to the task at hand
- Prefer editing existing files over creating new ones
- Update this file whenever the project structure changes significantly
- Keep all commands in this file executable and up to date
- Commit with clear messages; push to the designated feature branch

### DON'T

- Push to `main` or `master` directly
- Create a pull request unless explicitly asked to do so
- Commit secrets, credentials, or `.env` files
- Add speculative abstractions or features not explicitly requested
- Skip the linter/formatter before committing (once configured)
- Add comments that just restate what the code does — only comment on non-obvious WHY

---

## Updating This File

When the codebase grows, replace the placeholder sections above with accurate, executable information:

1. **Repository Overview** — describe what the project actually does; update the directory tree
2. **Development Setup** — exact commands to get a local environment running
3. **Testing** — exact commands and any environment requirements
4. **Linting and Formatting** — exact commands used in CI
5. **Code Conventions** — language-specific patterns and project style decisions
6. **CI/CD** — pipeline structure, checks, and deployment targets
