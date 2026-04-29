# OctoAcme — Risk Register Template

## Purpose
Provide a structured, reusable template for identifying, assessing, and tracking project risks throughout the lifecycle. This template aligns with the risk management guidance in [Risk Management & Communication](octoacme-risks-and-communication.md).

## When to Use
- **Initiation**: capture initial risks identified during the project one-pager review.
- **Planning**: expand and refine risks; assign owners and define mitigations.
- **Execution**: review and update at every weekly sync.
- **Release**: confirm all high/medium risks are resolved or have active mitigations before go-live.

## Risk Register Table Template

Copy the table below into your project's `docs/risk-register.md` and populate each row.

| ID | Date Identified | Description | Category | Impact (H/M/L) | Likelihood (H/M/L) | Risk Score | Owner | Mitigation Plan | Contingency Plan | Status |
|----|-----------------|-------------|----------|-----------------|---------------------|------------|-------|-----------------|------------------|--------|
| R-001 | YYYY-MM-DD | Short description | Schedule / Scope / Technical / Resource / External | H / M / L | H / M / L | (see matrix) | Name | Actions to reduce likelihood or impact | What to do if risk occurs | Open / Mitigated / Closed |

## Risk Score Matrix

Use the matrix below to derive a combined risk score from Impact × Likelihood.

| | **High Impact** | **Medium Impact** | **Low Impact** |
|---|---|---|---|
| **High Likelihood** | 🔴 Critical | 🟠 High | 🟡 Medium |
| **Medium Likelihood** | 🟠 High | 🟡 Medium | 🟢 Low |
| **Low Likelihood** | 🟡 Medium | 🟢 Low | 🟢 Low |

## Column Definitions

| Column | Guidance |
|--------|----------|
| **ID** | Sequential identifier (R-001, R-002 …) |
| **Date Identified** | ISO date the risk was first raised |
| **Description** | One- or two-sentence description of the risk event |
| **Category** | Schedule, Scope, Technical, Resource, External, Security, or Other |
| **Impact** | Consequence if the risk occurs: High, Medium, or Low |
| **Likelihood** | Probability the risk will occur: High, Medium, or Low |
| **Risk Score** | Derived from the matrix above |
| **Owner** | Team member responsible for monitoring and acting on this risk |
| **Mitigation Plan** | Steps taken to reduce likelihood or impact *before* the risk occurs |
| **Contingency Plan** | Steps to take *if* the risk materialises |
| **Status** | Open (being monitored), Mitigated (plan in place, reduced score), Closed (no longer relevant) |

## Example Entries

| ID | Date Identified | Description | Category | Impact | Likelihood | Risk Score | Owner | Mitigation Plan | Contingency Plan | Status |
|----|-----------------|-------------|----------|--------|------------|------------|-------|-----------------|------------------|--------|
| R-001 | 2025-06-10 | Key engineer may leave mid-project due to competing offer | Resource | H | M | 🟠 High | PM | Document knowledge, cross-train second engineer | Engage contractor; adjust scope for reduced capacity | Open |
| R-002 | 2025-06-12 | Third-party API rate limits may block integration testing | Technical | M | H | 🟠 High | Tech Lead | Request raised tier with vendor; build request throttling | Use mock API for CI; delay live integration to final sprint | Mitigated |
| R-003 | 2025-07-01 | Release date conflicts with company-wide freeze | Schedule | H | L | 🟡 Medium | PM | Monitor freeze calendar; align milestone dates early | Shift release to next available window; notify stakeholders | Open |

## Risk Review Cadence
- Review the register at every **weekly sync** — update Status, reassess scores if circumstances change.
- Surface any 🔴 Critical or 🟠 High risks immediately to the PM and Product Lead.
- Close risks that are no longer relevant; do not delete them (history matters for retrospectives).

## Related Documents
- [Risk Management & Communication](octoacme-risks-and-communication.md) — escalation paths and communication templates
- [Project Planning](octoacme-project-planning.md) — initial risk identification during planning
- [Weekly Status Update Template](octoacme-templates-status-update.md) — include top risks in weekly updates
- [Project Management Overview](octoacme-project-management-overview.md)
