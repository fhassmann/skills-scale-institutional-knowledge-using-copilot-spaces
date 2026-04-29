# OctoAcme — Weekly Project Status Update Template

## Purpose
Provide a concise, consistent format for weekly project status updates. Regular updates keep stakeholders informed, surface blockers early, and create a lightweight audit trail of project progress. This template aligns with the communication guidance in [Risk Management & Communication](octoacme-risks-and-communication.md).

## When to Send
- **Frequency:** Weekly (recommended: every Friday or the last working day of the week).
- **Audience:** PM, PdM, tech lead, and any stakeholders who need visibility.
- **Medium:** Email, Slack/Teams message, or a linked issue/comment in GitHub — use whatever channel your team has agreed on.

## Status Indicators

Use one of the following to set the overall health at a glance:

| Indicator | Meaning |
|-----------|---------|
| 🟢 **On Track** | Delivery is progressing as planned; no significant risks or blockers |
| 🟡 **At Risk** | One or more concerns may affect timeline or quality; mitigation in progress |
| 🔴 **Off Track** | Delivery is blocked or timeline is likely to slip; escalation required |

---

## Weekly Status Update Template

```
## [Project Name] — Weekly Status Update
**Week ending:** YYYY-MM-DD
**Overall Status:** 🟢 On Track / 🟡 At Risk / 🔴 Off Track
**PM:** [Name]  |  **Report #:** [N]

---

### Summary
[2–3 sentences: what the project is delivering, current phase, and high-level health.]

---

### Progress This Week
- [Completed item 1 — link to PR/issue if available]
- [Completed item 2]
- [Completed item 3]

### Planned for Next Week
- [Upcoming item 1]
- [Upcoming item 2]
- [Upcoming item 3]

---

### Milestones

| Milestone | Target Date | Status |
|-----------|-------------|--------|
| [Milestone 1] | YYYY-MM-DD | ✅ Done / 🔄 In Progress / ⏳ Not Started |
| [Milestone 2] | YYYY-MM-DD | |

---

### Top Risks & Blockers

| ID | Description | Impact | Status | Owner |
|----|-------------|--------|--------|-------|
| R-XXX | [Risk description] | H/M/L | Open / Mitigated | [Name] |

*(See [Risk Register](risk-register.md) for full details.)*

---

### Decisions Needed / Asks
- [ ] [Decision or action required from stakeholders — include deadline if any]
- [ ] [Another ask]

---

### Key Decisions Made This Week
- [D-XXX] [Short summary of decision] *(see [Decision Log](decisions.md))*

---

### Notes / Additional Context
[Anything else the audience should know — upcoming leave, dependencies on other teams, etc.]
```

---

## Example: Completed Status Update

```
## OctoAcme Payments — Weekly Status Update
**Week ending:** 2025-07-11
**Overall Status:** 🟡 At Risk
**PM:** Alex Kim  |  **Report #:** 6

---

### Summary
The Payments integration is in sprint 3 of 5. Core checkout flow is complete;
payment provider integration is blocked on vendor API credentials. Timeline
is at risk if credentials are not received by Wednesday.

---

### Progress This Week
- ✅ Checkout UI implemented and reviewed (PR #42)
- ✅ Unit tests added for cart logic (coverage now 84%)
- 🔄 Payment provider integration — backend in progress

### Planned for Next Week
- Complete payment provider integration (unblocked by credentials)
- E2E test pass on staging
- Draft release notes

---

### Milestones

| Milestone | Target Date | Status |
|-----------|-------------|--------|
| Checkout UI complete | 2025-07-04 | ✅ Done |
| Payment integration complete | 2025-07-18 | 🔄 In Progress |
| Beta release | 2025-08-01 | ⏳ Not Started |

---

### Top Risks & Blockers

| ID | Description | Impact | Status | Owner |
|----|-------------|--------|--------|-------|
| R-002 | Vendor API credentials not received — blocks integration | H | Open | Alex Kim |

*(See risk-register.md for full details.)*

---

### Decisions Needed / Asks
- [ ] **[by Wed 2025-07-16]** Legal to confirm vendor NDA signed so credentials can be shared

---

### Key Decisions Made This Week
- [D-004] Agreed to use vendor sandbox environment for CI to unblock testing

---

### Notes / Additional Context
Team has one member on leave 14–18 July; capacity reduced ~20%.
```

---

## Tips
- Keep updates to one page or a single Slack message — brevity is valued.
- Link directly to the Risk Register and Decision Log rather than duplicating content.
- If status is 🔴 Off Track, send an interim update mid-week rather than waiting for Friday.

## Related Documents
- [Risk Management & Communication](octoacme-risks-and-communication.md) — escalation paths and incident communication
- [Risk Register Template](octoacme-templates-risk-register.md) — full risk detail
- [Decision Log Template](octoacme-templates-decision-log.md) — full decision history
- [Project Management Overview](octoacme-project-management-overview.md)
