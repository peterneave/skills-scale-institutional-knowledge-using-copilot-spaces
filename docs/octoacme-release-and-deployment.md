# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted
- Rollback / mitigation plan documented
- Smoke tests prepared

## Deployment Checklist
- [ ] Deployment window scheduled (if needed)
- [ ] Backup or snapshot (if applicable)
- [ ] Deploy to staging and run smoke tests
- [ ] Stakeholder communication sent (release notes, timing, impacts, support contacts)
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Run post-deploy verifications
- [ ] Announce release to stakeholders and support

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items

### Expanded Rollback Procedures
When issues arise post-deployment, follow this playbook:

1. **Detect & Assess** (0-5 minutes)
   - Identify the issue via monitoring alerts or user reports
   - Assess severity: Does this require immediate rollback?
   - Declare incident if customer-impacting or data integrity at risk

2. **Communicate** (5-10 minutes)
   - Notify incident channel and on-call team
   - Update status page if customer-facing
   - Alert stakeholders on severity and expected timeline

3. **Rollback Decision** (10-15 minutes)
   - **Rollback if**: Critical functionality broken, data corruption, security vulnerability
   - **Don't rollback if**: Minor UI issue, non-critical feature flag can disable issue
   - Document decision and rationale in incident log

4. **Execute Rollback** (15-30 minutes)
   - Trigger automated rollback pipeline (preferred) or manual rollback steps
   - Verify rollback success via smoke tests
   - Confirm monitoring shows normal behavior
   - Update status page and notify stakeholders

5. **Post-Incident Review** (Within 48 hours)
   - Schedule blameless post-mortem with all involved parties
   - Use the 5 Whys or similar technique to identify root cause
   - Document timeline, impact, and contributing factors
   - Create action items to prevent recurrence

6. **Root Cause Analysis Documentation**
   - **What happened**: Detailed timeline of events
   - **Impact**: Affected users, duration, business impact metrics
   - **Root cause**: Technical and process factors that contributed
   - **Contributing factors**: Why wasn't this caught earlier? What signals were missed?
   - **Action items**: Specific, measurable improvements with owners and due dates
   - **Follow-up**: Schedule review of action items in 2-4 weeks

### Post-Incident Review Template
```
## Incident: [Title]
- **Date**: YYYY-MM-DD
- **Severity**: Critical / High / Medium / Low
- **Duration**: Start time → Resolution time
- **Impact**: Number of users affected, key functionality impacted

### Timeline
- [Time]: Event description
- [Time]: Action taken
- [Time]: Resolution

### Root Cause
[Detailed explanation of what caused the issue]

### Contributing Factors
- Technical: [e.g., Missing test coverage, configuration error]
- Process: [e.g., Insufficient review, unclear rollback procedure]
- Communication: [e.g., Alert fatigue, unclear escalation path]

### Action Items
- [ ] [Action] - Owner: [Name] - Due: [Date]
- [ ] [Action] - Owner: [Name] - Due: [Date]

### Lessons Learned
- What went well:
- What could be improved:
```

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
