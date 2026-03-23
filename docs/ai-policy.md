# AI Policy Baseline

## Scope

Applies to:
- AI features shipped by this project
- AI-assisted development workflows used by contributors

## Core Principles

- Human accountability: humans remain responsible for shipped outcomes.
- Transparency: disclose material AI usage in PRs and docs.
- Safety by design: evaluate risks before release.
- Privacy and security: minimize data exposure to third-party providers.
- Auditability: keep records for significant decisions and incidents.

## Minimum Requirements

1. Risk classification is required before shipping AI functionality.
2. High-risk changes require explicit maintainer approval.
3. AI-generated code/content must be human-reviewed.
4. Sensitive data must not be pasted into external AI tools without approval.
5. Incidents must be handled using `docs/incident-response.md`.

## Prohibited Practices

- Shipping unreviewed AI-generated code.
- Misleading users about AI capabilities or certainty.
- Using unapproved providers for sensitive workloads.

## Exceptions

Policy exceptions must be documented with rationale, scope, expiration date,
and owner using the policy exception issue template.
