# Shared Rules

These rules apply to all projects that include this submodule.

## General

- Read the project's own CLAUDE.md first. It takes precedence over these shared rules.
- Understand existing code before modifying it. Never propose changes to code you haven't read.
- Keep changes focused. Only do what was asked. Don't refactor, add docs, or "improve" surrounding code.
- Don't over-engineer. Prefer simple, direct solutions over abstractions for hypothetical futures.

## Code Quality

- Don't introduce security vulnerabilities (injection, XSS, SSRF, etc.).
- Validate at system boundaries (user input, external APIs). Trust internal code.
- Delete unused code. No backwards-compatibility shims, re-exports, or `// removed` comments.
- Follow the project's existing patterns, formatting, and naming conventions.

## Testing

- Follow TDD when working with the ralph skill chain.
- Tests describe behavior, not implementation. Don't over-mock.
- Don't create separate tasks for unit tests; they're part of each implementation task.

## Git

- Don't commit unless explicitly asked or a skill directs you to.
- Branch names are prefixed with the GitHub issue number (e.g., `123-feature-name`).
- Write concise commit messages that explain *why*, not *what*.

## Skills & Prompts

Shared skills live in `prompts/`. Use the appropriate skill for the task:
- `scope` — break a design into atomic, achievable tasks
- `ralph-code` — implement code (TDD green phase)
- `ralph-test` — write tests (TDD red phase)
- `ralph-refactor` — refactor code (TDD refactor phase)
- `ralph-pr` — prepare and open a pull request
- `pr-create` — create a pull request
- `ralph-next` — pick up the next task

Language expertise is available in `prompts/language-pros/`.
