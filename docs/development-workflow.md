# Development Workflow

This document describes the team's development workflow, including branching strategy, PR review process, CI/CD considerations, and coding standards.

## Branching Strategy

We use a **trunk-based** workflow with short-lived feature branches.

- **`main`** — Production-ready code. Always stable.
- **Feature branches** — Created from `main` for each task or issue. Named as `<author>/short-description` (e.g., `joey/add-development-workflow`).
- **No long-lived branches** — Merge back to `main` quickly to minimize drift.

### Branch Naming Convention

```
<author>/<brief-description>
```

Examples:
- `joey/add-development-workflow`
- `boy/research-methodology`
- `roey/fix-typo-in-readme`

## PR Review Process

1. **Create a branch** from `main` for your work.
2. **Make focused commits** — each commit should represent a logical unit of change.
3. **Open a Pull Request** referencing the related issue (e.g., "Closes #2").
4. **Request review** from at least one team member.
5. **Address feedback** — push additional commits to the same branch.
6. **Merge** once approved. Use squash merge for single-purpose PRs, merge commit for multi-step work.
7. **Delete the branch** after merging.

### PR Guidelines

- Keep PRs small and focused — one issue per PR when possible.
- Write a clear description: what changed and why.
- Include screenshots or examples if the change is visual or behavioral.
- Link the related issue in the PR body.

## CI/CD Considerations

- **Pre-merge checks** — All PRs should pass automated checks before merging.
- **Linting and formatting** — Enforced via pre-commit hooks or CI pipeline.
- **Tests** — Run the full test suite on every PR. Do not merge with failing tests.
- **Deployment** — Merges to `main` trigger automatic deployment to the staging environment. Production deploys require manual approval.

## Coding Standards and Conventions

### General

- Write clear, self-documenting code. Use comments only when the logic isn't obvious.
- Prefer simplicity over cleverness.
- Follow the principle of least surprise — code should do what a reader expects.

### Commits

- Use imperative mood in commit messages: "Add feature" not "Added feature".
- Keep the first line under 72 characters.
- Reference issue numbers when applicable.

### File Organization

- Place documentation in the `docs/` directory.
- Keep related files close together.
- Avoid deeply nested directory structures.

### Code Review Etiquette

- Be constructive and specific in feedback.
- Approve when satisfied — don't block on nitpicks.
- Respond to reviews within 24 hours.
