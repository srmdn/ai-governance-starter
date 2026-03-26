# Versioning

Projects using this starter should follow Semantic Versioning (semver): `vMAJOR.MINOR.PATCH`

## Rules

| Segment | Bump when... | Example |
|---|---|---|
| `MAJOR` | Breaking change — removes a feature, renames a flag, incompatible output or API | `v1.0.0` → `v2.0.0` |
| `MINOR` | New feature, backwards compatible | `v0.1.0` → `v0.2.0` |
| `PATCH` | Bug fix, backwards compatible, no new features | `v0.1.0` → `v0.1.1` |

## `v0.x.x` vs `v1.0.0`

- `v0.x.x` — early/unstable. API and behavior can still change freely.
- `v1.0.0` — stable. Commit to backwards compatibility on MAJOR bumps.

Cut `v1.0.0` when the project is deployed, tested in real use, and the public interface is settled.

## Git Tags

```bash
# Lightweight tag
git tag v0.2.0
git push origin v0.2.0

# Annotated tag (preferred — stores tagger, date, message)
git tag -a v0.2.0 -m "v0.2.0: short description of release"
git push origin v0.2.0
```

Annotated tags are preferred for releases — they carry metadata and show up properly in `git log` and GitHub release pages.

## CHANGELOG

Every release should have a `CHANGELOG.md` entry. Newest version at top:

```markdown
## v0.2.0 — 2026-03-26

- Added X feature
- Fixed Y bug

## v0.1.0 — 2026-03-01

- Initial release
```

Keep entries concise — one line per change. The git log fills in the detail.

## AI-Assisted Releases

When using AI tools to prepare a release:

- Human reviews and approves the version bump decision
- Human writes or approves the CHANGELOG entry
- Human runs `git tag` and `git push` — do not automate tag creation
- Commit messages must be human-authored (see `CONTRIBUTING.md`)
