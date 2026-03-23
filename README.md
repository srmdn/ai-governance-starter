# AI Governance Starter

A practical starter kit for running an open-source project that uses AI responsibly.

This repository provides policy, process, and templates for:
- transparent AI-assisted development
- risk classification and review
- model/provider standards
- incident reporting and response
- governance decisions with traceable records

## Who This Is For

Use this starter if your project:
- ships features powered by AI models, or
- uses AI heavily in software development and wants clear disclosure rules.

## Repository Structure

- `GOVERNANCE.md`: project roles, decision model, and voting/escalation rules
- `CONTRIBUTING.md`: contribution process, including AI-use disclosure requirements
- `SECURITY.md`: security reporting policy and SLAs
- `CODE_OF_CONDUCT.md`: expected community behavior
- `docs/ai-policy.md`: AI usage and safety baseline policy
- `docs/risk-assessment-rubric.md`: risk tiers and control requirements
- `docs/model-provider-standards.md`: provider/model selection checklist
- `docs/incident-response.md`: AI incident process
- `docs/decisions/`: architecture/policy decision records
- `.github/`: issue and pull request templates

## Quick Start

1. Copy this repository (or use it as a template).
2. Update project metadata and owner names in `GOVERNANCE.md` and `SECURITY.md`.
3. Decide your minimum controls in `docs/risk-assessment-rubric.md`.
4. Enforce PR disclosure via `.github/pull_request_template.md`.
5. Begin recording key governance choices in `docs/decisions/`.

## Suggested Workflow

1. Classify each new AI feature by risk tier.
2. Document model/provider choice and safety controls.
3. Require contributor AI-use disclosure in each PR.
4. Capture major decisions with a decision record.
5. Run periodic governance review and publish outcomes.

## License

MIT (see `LICENSE`).
