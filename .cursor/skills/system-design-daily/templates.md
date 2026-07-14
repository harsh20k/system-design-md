# Templates

## Day question file

Path: `Docs/Day {N} SysDesign Question {N}.md`

```markdown
# Day {N} — {Topic}

**Date:** YYYY-MM-DD
**Topic:** {Topic}
**Difficulty band:** fundamentals | aws-sap-c02 | mock-interview
**Linear:** {issue URL or identifier}

## Question

{scenario 3–5 sentences with constraints}

## Answer (Harsh)

_Pending_

## Feedback

_Pending_

## Architecture diagram

_Pending — generate via aws-architecture-diagram after answer_
```

## Question-Index.md

Path: `Docs/Question-Index.md`

Create if missing with this header, then append one row per day:

```markdown
# System Design Question Index

| Day | Topic | File | Linear | Diagram |
|-----|-------|------|--------|---------|
| {N} | {Topic} | [Day {N}](Day%20{N}%20SysDesign%20Question%20{N}.md) | {id or link} | — |
```

When a diagram exists, replace `—` with a link to the `.drawio` under `docs/`.

## Linear issue

- **title:** `Day {N} — {Topic}`
- **description:** same text as the Question section (markdown)
- **team:** `MasterChief-life`
- **project:** `System-Design.md`
