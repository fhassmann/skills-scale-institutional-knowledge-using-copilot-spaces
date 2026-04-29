# OctoAcme — Definition of Done & Acceptance Criteria Template

## Purpose
Provide a shared, reusable Definition of Done (DoD) and acceptance criteria checklist so the team has a consistent, unambiguous standard for "complete" work. This template aligns with [Project Planning](octoacme-project-planning.md) and [Execution & Tracking](octoacme-execution-and-tracking.md).

## Definition of Done (DoD)

The DoD applies to **every user story or backlog item** unless explicitly overridden. Copy and adapt the list below for your project during planning kickoff.

### Code Quality
- [ ] Code reviewed and approved by at least one peer
- [ ] No high or critical lint/static-analysis warnings introduced
- [ ] Code follows team naming and style conventions
- [ ] No `TODO` or `FIXME` comments left unresolved in new code

### Testing
- [ ] Unit tests written for all new logic (target: ≥ 80% coverage for new code)
- [ ] Integration tests updated or added where applicable
- [ ] All existing automated tests pass in CI
- [ ] Manual QA completed for UI or user-facing flows (if applicable)
- [ ] Edge cases and error states covered

### Security & Compliance
- [ ] No new high/critical security findings from automated scanning (e.g., CodeQL, Dependabot)
- [ ] Sensitive data (credentials, PII) not exposed in logs or responses
- [ ] Access controls validated for new endpoints or data mutations

### Documentation
- [ ] Public API or configuration changes reflected in docs
- [ ] README or relevant process doc updated if workflow changes
- [ ] Release notes entry drafted (if feature-level)

### Deployment Readiness
- [ ] Feature flag added if partial rollout is needed
- [ ] Database migrations tested against a realistic dataset
- [ ] Rollback procedure documented for breaking changes
- [ ] Monitoring/alerting configured for new critical paths

### Acceptance
- [ ] All acceptance criteria for the specific story met (see checklist below)
- [ ] Demo completed and signed off by Product Manager or designated stakeholder

---

## Acceptance Criteria Checklist Template

Use this per-story checklist alongside or in place of free-form acceptance criteria text. Add it to the issue or PR description.

### Story: [Story Title]

**User Story:** As a [persona], I want [goal] so that [benefit].

#### Functional Criteria
- [ ] [Criterion 1 — observable behaviour or outcome]
- [ ] [Criterion 2]
- [ ] [Criterion 3]

#### Non-Functional Criteria
- [ ] Performance: [specific threshold, e.g., page loads in < 2 s on 3G]
- [ ] Accessibility: [e.g., passes WCAG 2.1 AA for new UI elements]
- [ ] Localisation: [e.g., all new strings are internationalised]

#### Out of Scope
- [List anything explicitly excluded to prevent scope creep]

#### Test Scenarios

| # | Given | When | Then |
|---|-------|------|------|
| 1 | [precondition] | [action] | [expected result] |
| 2 | | | |

---

## Example: Completed DoD & Acceptance Criteria

**Story:** As a project manager, I want a weekly status email so that stakeholders are informed without attending every meeting.

#### Functional Criteria
- [ ] System sends email every Monday at 09:00 in the PM's configured timezone
- [ ] Email includes: progress summary, blockers, and top 3 risks
- [ ] PM can configure recipient list in project settings

#### Non-Functional Criteria
- [ ] Email delivers within 5 minutes of scheduled time (P99)
- [ ] Unsubscribe link present and functional

#### Test Scenarios

| # | Given | When | Then |
|---|-------|------|------|
| 1 | PM has configured 3 recipients | Monday 09:00 arrives | All 3 recipients receive the email |
| 2 | PM removes a recipient before Monday 09:00 | Monday 09:00 arrives | Removed recipient does not receive the email |

---

## Adapting the DoD

- Review and adjust the DoD during **planning kickoff** and update it after retrospectives.
- Record any project-specific changes in the project's decision log (see [Decision Log Template](octoacme-templates-decision-log.md)).
- A lightweight project may reduce the DoD; a regulated/high-risk project may add checks.

## Related Documents
- [Project Planning](octoacme-project-planning.md) — DoD is defined during planning
- [Execution & Tracking](octoacme-execution-and-tracking.md) — DoD is applied during sprint execution
- [Release Readiness Checklist](octoacme-templates-release-readiness.md) — release-level quality gate
- [Project Management Overview](octoacme-project-management-overview.md)
