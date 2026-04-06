# ai-governance-starter

Reusable starter kit for AI-assisted open source projects. Very useful starter-kit

## Design Goals

1. Model-agnostic governance (Claude, ChatGPT, Codex, and others)
2. No AI branding/co-author commit trailers in git history
3. Contributor-friendly enforcement with clear recovery steps
4. Ready-to-copy templates for other repos

## Included Files

- `AGENTS.md`
- `CLAUDE.md`
- `.env.example`
- `CONTRIBUTING.md`
- `SECURITY.md`
- `CODEOWNERS`
- `.github/pull_request_template.md`
- `.gitlab/merge_request_templates/Default.md`
- `scripts/check-commit-attribution.sh`
- `scripts/pre-commit` (git hook for local enforcement)
- `.github/workflows/commit-attribution-check.yml`
- `.gitlab-ci.yml`
- `docs/AI-COMMIT-CLEANUP.md`
- `docs/gitignore.md`
- `docs/business-ai-policy.md`
- `docs/ai-procurement-checklist.md`
- `docs/go-to-market-risk-checklist.md`

## Quick Start

```sh
git clone <this-repo>
cd ai-governance-starter

# Install the pre-commit hook (local enforcement)
cp scripts/pre-commit .git/hooks/pre-commit
chmod +x .git/hooks/pre-commit

# Run the attribution check manually
scripts/check-commit-attribution.sh HEAD
```

## Copy Into an Existing Repo

```sh
cp .gitignore .env.example AGENTS.md CLAUDE.md CONTRIBUTING.md SECURITY.md CODEOWNERS /path/to/repo/
mkdir -p /path/to/repo/scripts /path/to/repo/docs
cp scripts/check-commit-attribution.sh /path/to/repo/scripts/
cp docs/AI-COMMIT-CLEANUP.md /path/to/repo/docs/
mkdir -p /path/to/repo/.github/workflows /path/to/repo/.gitlab/merge_request_templates
cp .github/pull_request_template.md /path/to/repo/.github/
cp .github/workflows/commit-attribution-check.yml /path/to/repo/.github/workflows/
cp .gitlab/merge_request_templates/Default.md /path/to/repo/.gitlab/merge_request_templates/
cp .gitlab-ci.yml /path/to/repo/
```

Then customize project-specific fields:
- contacts in `SECURITY.md`
- owners in `CODEOWNERS`
- reviewer/escalation expectations in `CONTRIBUTING.md`

## Local One-Step Test

```sh
scripts/check-commit-attribution.sh HEAD
```

## Related

**[ai-dev-playbook](https://gitlab.com/srmdn/ai-dev-playbook)** — practical day-to-day guide for working efficiently with AI coding assistants: token optimization, session hygiene, git workflow, tool switching, and when not to use AI. Complements this repo's governance rules.

## License

MIT
