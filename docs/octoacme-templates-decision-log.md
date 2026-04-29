# OctoAcme — Decision Log Template

## Purpose
Record key project decisions so the team has a durable, searchable history of *what* was decided, *why*, and *by whom*. This prevents revisiting settled questions and gives new team members essential context.

## Where to Keep the Decision Log
- Store the decision log in the project repository under `docs/` (e.g., `docs/decisions.md`) or as a linked page in the team wiki.
- Reference it from the project one-pager so stakeholders know where to find it.
- Update it in real time — decisions should be logged within 24 hours of being made.

## Decision Log Table Template

Copy the table below into your project's `docs/decisions.md` file and add one row per decision.

| ID | Date | Title | Context | Decision | Alternatives Considered | Outcome / Status | Owner |
|----|------|--------|---------|----------|------------------------|------------------|-------|
| D-001 | YYYY-MM-DD | Short title | Brief description of the problem or question | What was decided | Other options evaluated | Open / Accepted / Superseded | Name |

## Column Definitions

| Column | Guidance |
|--------|----------|
| **ID** | Sequential identifier (D-001, D-002 …) for easy reference in other docs |
| **Date** | ISO date the decision was finalized |
| **Title** | One-line summary (e.g., "Use PostgreSQL as primary datastore") |
| **Context** | Why a decision was needed — constraints, requirements, or competing forces |
| **Decision** | The choice that was made, stated clearly |
| **Alternatives Considered** | Other options and a short reason they were not chosen |
| **Outcome / Status** | Open (pending), Accepted (in effect), or Superseded (replaced by a later decision) |
| **Owner** | Person accountable for the decision |

## Example Entries

| ID | Date | Title | Context | Decision | Alternatives Considered | Outcome / Status | Owner |
|----|------|--------|---------|----------|------------------------|------------------|-------|
| D-001 | 2025-06-10 | Adopt GitHub Projects for tracking | Team needed a single board visible to all contributors | Use GitHub Projects (v2) | Jira (licensing cost), Linear (unfamiliar to team) | Accepted | PM |
| D-002 | 2025-06-18 | Skip staging environment for v0.1 | Timeline pressure; feature is internal-only | Deploy directly to production with feature flags | Full staging env (build time), canary (complexity) | Accepted | Tech Lead |
| D-003 | 2025-07-02 | Revisit D-002 — add staging for v0.2 | Post-launch incidents linked to missing staging | Introduce staging pipeline before v0.2 | Continue feature flags only | Supersedes D-002 | PM |

## Tips
- Link decision IDs in PR descriptions and issue comments (e.g., `see D-001`).
- Revisit and mark decisions as **Superseded** rather than deleting them — history matters.
- If a decision is highly technical (e.g., architecture choice), consider a full Architecture Decision Record (ADR) and link it from this log.

## Related Documents
- [Risk Management & Communication](octoacme-risks-and-communication.md) — decisions about risk mitigations should also appear in the Risk Register
- [Project Planning](octoacme-project-planning.md) — record planning-phase decisions early
- [Project Management Overview](octoacme-project-management-overview.md)
