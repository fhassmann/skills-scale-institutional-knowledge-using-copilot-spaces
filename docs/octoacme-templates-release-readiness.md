# OctoAcme — Release Readiness Checklist

## Purpose
Provide an expanded, go/no-go quality gate before every production release. This checklist ties together the execution, testing, and communication requirements from [Execution & Tracking](octoacme-execution-and-tracking.md) and the deployment steps in [Release & Deployment](octoacme-release-and-deployment.md).

## When to Use
Complete this checklist before triggering any production deployment. For hotfix/patch releases, sections that do not apply may be marked N/A with a short justification.

---

## Release Readiness Checklist

**Release name / version:** _______________  
**Target release date:** YYYY-MM-DD  
**Release owner:** _______________  
**Checklist completed by:** _______________ on YYYY-MM-DD  

---

### 1. Scope & Acceptance

- [ ] All stories/issues in the release milestone are in **Done** status or explicitly deferred (documented)
- [ ] Every item meets the [Definition of Done](octoacme-templates-definition-of-done.md)
- [ ] Product Manager has signed off on acceptance criteria for all user-facing changes
- [ ] Breaking changes or deprecations are identified and communicated

### 2. Code & Build Quality

- [ ] All PRs for this release are merged to the release branch
- [ ] No high or critical lint/static-analysis warnings on the release branch
- [ ] Build pipeline passes end-to-end (no failing steps)
- [ ] Dependencies are up-to-date; no known vulnerable packages (Dependabot alerts resolved)

### 3. Testing

- [ ] All automated unit and integration tests pass in CI
- [ ] End-to-end / smoke test suite passes on staging environment
- [ ] Manual QA sign-off completed for all user-facing changes
- [ ] Regression testing completed for affected areas
- [ ] Performance benchmarks meet defined thresholds (if applicable)
- [ ] Security scan (e.g., CodeQL, SAST) passes with no new high/critical findings
- [ ] Accessibility checks completed for new UI (if applicable)

### 4. Database & Data

- [ ] All database migrations tested against a realistic dataset on staging
- [ ] Migration rollback scripts written and tested
- [ ] No data loss risk identified; backup taken (if applicable)

### 5. Configuration & Feature Flags

- [ ] Environment-specific configuration (env vars, secrets) updated for production
- [ ] Feature flags set to the correct state for the release
- [ ] No hardcoded credentials or environment-specific values in code

### 6. Documentation & Release Notes

- [ ] Release notes drafted and reviewed (see [Release Notes Template](octoacme-release-and-deployment.md))
- [ ] API documentation updated (if public API changed)
- [ ] User-facing help docs or changelogs updated
- [ ] Internal runbooks updated for operational changes

### 7. Monitoring & Observability

- [ ] Alerts and dashboards configured for new critical paths
- [ ] Log levels appropriate for production (no excessive debug logging)
- [ ] SLO/SLA thresholds reviewed and still valid after this release

### 8. Rollback & Incident Response

- [ ] Rollback procedure documented and tested (or N/A for forward-only migrations — justify)
- [ ] On-call engineer notified of deployment window
- [ ] Incident runbook updated if operational behaviour changes
- [ ] Point of contact confirmed for release window

### 9. Stakeholder Communication

- [ ] Deployment window scheduled and communicated to relevant teams
- [ ] Customer-facing announcement or in-app message prepared (if applicable)
- [ ] Support team briefed on new features and known issues
- [ ] Release linked to corresponding GitHub milestone / issue for traceability

### 10. Go / No-Go Decision

| Reviewer | Role | Decision | Date |
|----------|------|----------|------|
| | PM | ☐ Go  ☐ No-Go | |
| | Tech Lead | ☐ Go  ☐ No-Go | |
| | QA Lead | ☐ Go  ☐ No-Go | |
| | PdM | ☐ Go  ☐ No-Go | |

> **Release is approved when all reviewers record Go.** Any No-Go must be resolved and the checklist re-reviewed before deployment.

---

## Post-Deployment Verification

After deploying to production, confirm the following within **30 minutes** of deployment:

- [ ] Deployment pipeline completed without errors
- [ ] Smoke tests pass against production
- [ ] Key user journeys verified manually (critical paths)
- [ ] Error rate and latency metrics within normal bounds
- [ ] Stakeholder announcement sent

If any post-deployment check fails, initiate the rollback procedure from [Release & Deployment](octoacme-release-and-deployment.md#rollback--incident-playbook).

---

## Related Documents
- [Release & Deployment](octoacme-release-and-deployment.md) — deployment steps and rollback playbook
- [Definition of Done & Acceptance Criteria](octoacme-templates-definition-of-done.md) — per-story quality standard
- [Risk Register Template](octoacme-templates-risk-register.md) — confirm release-blocking risks are resolved
- [Execution & Tracking](octoacme-execution-and-tracking.md) — testing and quality requirements during execution
- [Weekly Status Update Template](octoacme-templates-status-update.md) — communicate release status to stakeholders
- [Project Management Overview](octoacme-project-management-overview.md)
