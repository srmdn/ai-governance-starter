# Conventional Commits

This project follows the [Conventional Commits](https://www.conventionalcommits.org/) specification for commit messages.

## Format

```
<type>: <short description>

[optional body]

[optional footer]
```

## Types

| Type | Use for |
|---|---|
| `feat` | New feature |
| `fix` | Bug fix |
| `docs` | Documentation only |
| `refactor` | Code restructure, no behavior change |
| `perf` | Performance improvement |
| `test` | Adding or fixing tests |
| `chore` | Build process, tooling, dependencies |
| `ci` | CI/CD configuration changes |
| `revert` | Reverting a previous commit |

## Examples

```
feat: add HEAD→GET fallback for bot-hostile sites
fix: skip URLs inside fenced code blocks
docs: add versioning guide
refactor: extract URL deduplication into helper function
chore: update go.mod to Go 1.23
```

## Breaking Changes

Add `!` after the type for breaking changes:

```
feat!: change report format — Broken/OK/Skipped sections
fix!: rename --skip to --skip-pattern
```

Or add a `BREAKING CHANGE:` footer:

```
feat: restructure CLI flags

BREAKING CHANGE: --smtp-port now defaults to 587 instead of 465
```

Breaking changes bump the MAJOR version (see `docs/versioning.md`).

## Rules

- Use lowercase for type and description
- No period at the end of the description
- Keep the description under 72 characters
- No AI branding lines in commit messages (see `CONTRIBUTING.md`)

## Why This Matters

- Consistent history makes it easy to scan what changed and why
- Tooling (e.g. git-cliff) can auto-generate CHANGELOG from conventional commits
- Reviewers and future maintainers can understand intent at a glance
