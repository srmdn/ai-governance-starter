# Releases

This document covers the difference between git tags and GitHub/GitLab releases, and when to use each.

## Git Tag vs GitHub Release

| | Git Tag | GitHub/GitLab Release |
|---|---|---|
| What it is | A named pointer to a commit | A tag + release notes + optional file attachments |
| Where it lives | Git history | Repo's Releases page |
| Use case | Any project | Tools and apps users install or download |
| Required for `go install` | Yes | No |
| Visible to non-technical users | No | Yes |

**Rule of thumb:**
- Docs-only repos: git tag is enough (or skip tags entirely)
- Tools and apps with users: create a GitHub/GitLab Release

## Creating a GitHub Release

After tagging:

```bash
git tag -a v0.2.0 -m "v0.2.0: brief description"
git push origin v0.2.0
```

Then on GitHub:
1. Go to **Releases** → **Draft a new release**
2. Select the tag
3. Title: `v0.2.0`
4. Body: paste the relevant CHANGELOG section
5. Attach binaries if applicable
6. Publish

Or via `gh` CLI:

```bash
gh release create v0.2.0 --title "v0.2.0" --notes "$(cat <<'EOF'
## What's Changed

- Added X feature
- Fixed Y bug
EOF
)"
```

## Release Notes Format

Keep release notes readable for non-technical users:

```markdown
## What's Changed

- Added skip pattern support — skip URLs matching a regex (#12)
- Fixed false positives from code blocks (#10)
- Improved email report format

## How to Update

go install github.com/your/tool@v0.2.0

## Full Changelog

https://github.com/your/tool/compare/v0.1.0...v0.2.0
```

## Release Cadence

- No fixed schedule — release when you have something meaningful
- Don't tag every commit
- Group related fixes and features into one release
- Patch releases (`v0.1.1`) can be released quickly for critical fixes

## AI-Assisted Release Notes

AI tools can draft release notes from commit history:

```bash
git log v0.1.0..v0.2.0 --oneline
# paste output to AI, ask for release notes draft
```

Human reviews and edits before publishing. Human publishes the release — never automate.
