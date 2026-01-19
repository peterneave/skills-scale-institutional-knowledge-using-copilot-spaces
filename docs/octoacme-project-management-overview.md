# OctoAcme Project Management Overview

## Purpose
Provide a concise, shareable introduction to how OctoAcme runs projects so new teammates can quickly understand our approach, roles, and key artifacts.

## Scope
Applies to all cross-functional projects that deliver product features, services, or integrations.

## Principles
- Customer-first: prioritize customer value and usability.
- Iterative delivery: deliver small, testable increments.
- Clear ownership: each project has a named Project Manager (PM) and Product Lead.
- Data-informed decisions: measure impact and iterate based on evidence.
- Psychological safety: encourage feedback and learning.

## Core Roles
- Project Manager (PM): coordinates delivery, schedules, risk, communications.
- Product Manager (PdM): defines outcomes, prioritizes backlog, and measures success.
- Developers: implement features, collaborate on design and testability.
- QA/Testing: validate quality and acceptance criteria.
- Stakeholders: provide inputs and approvals.

## Key Artifacts
- Project Charter / One-pager
- Roadmap and Release Plan
- Sprint/Iteration Backlog
- Acceptance Criteria & Definition of Done
- Risk Register
- Retrospective notes and action items

## Lifecycle (high-level)
1. Initiation: problem statement, stakeholders, high-level timeline.
2. Planning: scope, resources, milestones, dependencies.
3. Execution: build, test, review, iterate.
4. Release: deploy, verify, announce.
5. Close & Retrospective: capture learnings and next steps.

### Project Lifecycle Diagram
```
┌─────────────┐
│  Initiation │  ← Problem identified, stakeholders aligned
└──────┬──────┘
       │ Decision Gate: Approved?
       ▼
┌─────────────┐
│   Planning  │  ← Scope defined, backlog created, timeline set
└──────┬──────┘
       │ Decision Gate: Ready to build?
       ▼
┌─────────────┐
│  Execution  │  ← Iterative development, testing, demos
└──────┬──────┘    (Loop back for additional iterations)
       │ Decision Gate: Ready to ship?
       ▼
┌─────────────┐
│   Release   │  ← Deploy to production, verify, announce
└──────┬──────┘
       │
       ▼
┌─────────────┐
│Retrospective│  ← Capture learnings, action items, celebrate
└─────────────┘
```

**Lifecycle Transition Checklist:**
- Initiation → Planning: Sponsor approval, stakeholder alignment, team commitment
- Planning → Execution: Backlog prioritized, Definition of Done agreed, kickoff complete
- Execution → Release: All acceptance criteria met, tests passing, rollback plan ready
- Release → Retrospective: Production deployment verified, stakeholders notified

## Communication Cadence
- Weekly sync between PM + PdM
- Twice-weekly standups for delivery team (or as agreed)
- Monthly stakeholder updates
- Ad-hoc escalations as needed

## Cross-Timezone & Remote Collaboration
OctoAcme teams operate across multiple timezones. To ensure effective collaboration:

### Async Meeting Best Practices
- Record all important meetings and share in the team channel
- Use written agendas and async pre-reads to reduce meeting time
- Document decisions immediately in the project tracker or README
- Allow 24-48 hours for async responses before escalating
- Use threaded discussions for context retention

### Preferred Communication Tools
- **Slack/Teams**: Real-time questions, quick updates, and daily standups
- **GitHub Discussions/Issues**: Technical decisions, feature specs, and long-lived threads
- **Confluence/Docs**: Documentation, project charters, and retrospectives
- **Video calls**: Weekly syncs, planning sessions, and demos (always recorded)
- **Email**: Formal stakeholder communications and approvals

### Timezone Considerations
- Rotate meeting times quarterly to share the inconvenience
- Maintain at least 3-hour overlap for synchronous collaboration
- Use "core hours" (e.g., 10 AM–2 PM in the most common timezone) for urgent matters
- Tag messages with urgency level: 🔴 Urgent (same day), 🟡 Normal (24-48h), 🟢 Low priority (when you can)

## How to use these docs
- Keep the Project Charter updated in the project repo.
- Add process-specific docs into `.copilot/` if you want Copilot Spaces to use them as context.
