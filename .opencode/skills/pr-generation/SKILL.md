---
name: pr-generation
description: PR title, PR description, and GitHub pull request body. Use when drafting or rewriting a pull request title/body from a change summary.
---

# PR Generation

Use this skill to write GitHub PR titles and descriptions that match the MODU convention.

## Title

- Format: `[TICKET]: short imperative summary`
- Put the ticket first, for example `MDU-38`, `MDU-X`, or `MDU-TEST`
- Keep it one line, factual, and outcome-focused
- Start with a verb such as `Add`, `Remove`, `Update`, `Rename`, `Complete`, or `Document`
- Avoid vague wording and avoid extra commentary

Examples:

- `[MDU-38]: Add demo product data source and repository implementation`
- `[MDU-X]: Rename Android application identity`

## Body

Use this structure:

```md
## Ticket
MDU-38

## Description
One sentence describing what changes and why.

## Development
Concrete implementation details, grouped by what was changed.

## Validation
- [x] Unit tests — 89 passed (`./gradlew testDebugUnitTest`)
- [x] Manual verification — tested on emulator API 34
```

## Rules

- If the ticket is missing, ask for it before writing the title
- Keep `Description` short and high-level
- Use `Development` for technical specifics, file areas, behavior changes, or ADRs
- Use `Validation` for observed test/build results that were run; do not list what was not run — absence implies not verified
- Keep the tone direct and factual
- Do not invent benefits or write marketing copy

## Default phrasing

- `Description`: what the change does and the reason it matters
- `Development`: how the code changed and why, if needed
- `Validation`: what was verified in this session
