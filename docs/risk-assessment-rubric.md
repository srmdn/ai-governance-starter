# Risk Assessment Rubric

Classify AI features using the highest applicable tier.

## Tier 0: Low Risk

Examples:
- non-user-facing internal tooling
- low-impact draft generation with full human review

Controls:
- basic testing
- PR AI disclosure

## Tier 1: Moderate Risk

Examples:
- user-facing summarization or recommendations
- automation that influences user workflows

Controls:
- prompt/output evaluation
- fallback behavior
- documented limitations

## Tier 2: High Risk

Examples:
- decisions affecting rights, safety, finances, or legal exposure
- features processing sensitive personal/business data

Controls:
- pre-release risk review by maintainers
- stronger monitoring and incident runbook
- explicit human override path
- decision record in `docs/decisions/`

## Tier 3: Critical Risk

Examples:
- safety-critical or heavily regulated use cases

Controls:
- formal approval gate
- staged rollout and kill switch
- security and legal review
- post-launch audit schedule
