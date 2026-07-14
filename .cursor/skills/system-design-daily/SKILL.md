---
name: system-design-daily
description: >-
  Delivers one daily System Design interview practice question tracked toward
  AWS Solutions Architect Professional (SAP-C02) via Linear project
  "System-Design.md". Use when the user says "system design question",
  "daily system design", "DSD", "SD practice", or similar.
---

# System Design Daily

Deliver **ONE** practice question per session. Search the internet when useful. Rotate topics across (SAP-C02 relevant): scalability, high availability/DR, microservices, databases (SQL/NoSQL/caching), messaging/queues, networking/VPC, security/IAM, cost optimization, migration strategy, multi-region, serverless, storage tiering.

## Paths & integrations

| Resource | Value |
|----------|-------|
| Project root | `/Users/harsh/Artifacts/system-design-md` |
| Docs folder | `Docs/` (under project root) |
| Question index | `Docs/Question-Index.md` |
| Diagrams | `docs/` (draw.io from aws-architecture-diagram skill) |
| Linear team | `MasterChief-life` |
| Linear project | `System-Design.md` |
| Diagram skill | Read and follow `aws-architecture-diagram` (deploy-on-aws plugin) |

Linear MCP (`plugin-linear-linear`):
- `list_issues` with `project: "System-Design.md"`, `team: "MasterChief-life"`
- `save_issue` to create (no `id`): `team`, `project`, `title`, `description`

## Topic rotation & difficulty

Round-robin through topics (see [topics.md](topics.md)). Skip topics already covered in Linear/Docs.

| Days | Level |
|------|-------|
| 1–14 (weeks 1–2) | Fundamentals — classic system design patterns |
| 15–35 (weeks 3–5) | AWS-specific SAP-C02 scenarios |
| 36–56 (weeks 6–8) | Full mock-interview multi-constraint problems |

Escalate constraints (scale, latency, budget, compliance) as days progress.

## Workflow

### 1. Check progress

1. `list_issues` on Linear project `System-Design.md` (team `MasterChief-life`).
2. Read `Docs/Question-Index.md` if it exists.
3. Compute next day **N** = max Day number found + 1 (start at 1 if empty).
4. Note topics already used — do not repeat the same topic+angle.

### 2. Pick next topic

Round-robin unused topics from the list. Match difficulty band to day N. Optionally web-search for a fresh SAP-C02-aligned angle.

### 3. Present ONE question (no answer)

Concise format only:

```markdown
## Day N — [Topic]

[Scenario: 3–5 sentences. Include constraints: scale, latency, budget, compliance where relevant.]
```

**Do NOT give the answer unless Harsh asks.**

### 4. Log the question

**A. Linear** — `save_issue`:
- `team`: `MasterChief-life`
- `project`: `System-Design.md`
- `title`: `Day N — [topic]`
- `description`: full question text (markdown, real newlines)

**B. Docs file** — create:

`Docs/Day N SysDesign Question N.md`

Use the template in [templates.md](templates.md).

**C. Index** — append a row/link to `Docs/Question-Index.md` (create file if missing).

### 5. If Harsh answers → brief feedback

Short, direct feedback only:
- Strengths
- Gaps vs AWS Well-Architected pillars (Operational Excellence, Security, Reliability, Performance Efficiency, Cost Optimization, Sustainability)
- No essay. No full model answer unless asked.

### 6. If Harsh wants a diagram (or after a substantial answer)

1. Read and follow the **aws-architecture-diagram** skill (Mode B brainstorm from Harsh's response).
2. Put a short **overview of the question** in the diagram title/subtitle block (top of diagram).
3. Save under project `docs/` (skill default).
4. Append to that day's `Docs/Day N SysDesign Question N.md`:
   - link to the `.drawio` file
   - preview URL if generated
   - optional notes from Harsh's answer / feedback summary

## Session rules

- **One question only** per trigger/session unless Harsh explicitly asks for another.
- Never spoil the answer up front.
- Prefer AWS services and trade-offs that map to SAP-C02.
- Keep presentation terse; Harsh prefers brief responses.
- Journal: append a short entry to `notes/journal/YYYY-MM-DD.journal.md` after delivering/logging a question (per user diary rule).

## Quick checklist

```
- [ ] Listed Linear issues + read Question-Index
- [ ] Chose topic (no repeat) + difficulty for Day N
- [ ] Presented question only (no answer)
- [ ] Created Linear issue Day N — [topic]
- [ ] Wrote Docs/Day N SysDesign Question N.md
- [ ] Updated Docs/Question-Index.md
- [ ] (If answered) Brief WA-pillar feedback
- [ ] (If diagram) aws-architecture-diagram + logged in day's .md
```
