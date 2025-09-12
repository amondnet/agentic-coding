# Agentic Coding

A comprehensive framework for AI-assisted software development with specialized agents and best practices for code quality, testing, and collaboration.

## Overview

This repository provides guidelines, tools, and specialized agents to enhance AI-powered coding workflows. It emphasizes clean code practices, security, thorough testing, and systematic problem-solving approaches.

## Key Components

### Core Documentation

- **AGENTS.md** - Comprehensive coding guidelines and rules for AI agents
- **CLAUDE.md** - Configuration for Claude Code integration
- **REVIEW.md** - Code review guidelines and standards
- **SUBAGENT.md** - Framework for creating and using specialized sub-agents

### Specialized Agents

Located in the `agents/` directory:

- **test-runner** - Executes tests and analyzes results with comprehensive logging
- **code-analyzer** - Deep-dive analysis for bug detection and code review
- **file-analyzer** - Analyzes and summarizes file contents efficiently
- **parallel-worker** - Executes parallel work streams in git worktrees

### Commands

Located in `.claude/commands/`:

- **commit-and-pr** - Automated commit and pull request creation
- **fix-issue** - Issue resolution workflow
- **review** - Code review automation

## Core Principles

### Mandatory Rules

1. **Read Before Changing**: Always read relevant files end-to-end before modifications
2. **Small Changes**: Keep tasks, commits, and PRs focused and minimal
3. **Document Assumptions**: Record all assumptions in Issues/PRs/ADRs
4. **Security First**: Never commit secrets or bypass input validation
5. **Clear Naming**: Use intention-revealing names throughout
6. **Compare Options**: Evaluate at least two approaches before deciding

### Development Workflow

1. **Problem Definition** → **Small, Safe Change** → **Change Review** → **Refactor** → **Repeat**

### Code Quality Standards

- Files ≤ 300 LOC
- Functions ≤ 50 LOC
- Parameters ≤ 5
- Cyclomatic complexity ≤ 10
- Explicit over implicit code
- Isolated side effects at boundaries

### Testing Requirements

- New code requires new tests
- Bug fixes must include regression tests
- Tests must be deterministic and independent
- Include both happy path and failure path scenarios
- Use fakes/contract tests for external systems

## Commit Convention

Following `@commitlint/config-conventional`:

```
<type>[optional scope]: <description>
```

**Allowed types**: `build`, `chore`, `ci`, `docs`, `feat`, `fix`, `perf`, `refactor`, `revert`, `style`, `test`

**Examples**:
- ✅ `fix: resolve memory leak in user service`
- ✅ `feat(auth): add OAuth2 integration`
- ❌ `Fix: Some Message.` (wrong case, ends with period)

## Security Guidelines

- Validate, normalize, and encode all inputs
- Use parameterized operations
- Apply Principle of Least Privilege
- Never log sensitive data
- Use structured logging with correlation IDs

## Getting Started

1. Review `AGENTS.md` for comprehensive coding guidelines
2. Configure your environment according to `CLAUDE.md`
3. Familiarize yourself with available agents in the `agents/` directory
4. Follow the commit conventions and review guidelines

## Contributing

1. Read and follow all guidelines in `AGENTS.md`
2. Write a Problem 1-Pager before implementing features
3. Ensure all tests pass before submitting PRs
4. Follow the review checklist in `REVIEW.md`
5. Use appropriate specialized agents for complex tasks

## License

[Specify your license here]