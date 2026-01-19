# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

## Team Rhythm
- Daily standups (15 min) — focus on progress, blockers, dependencies
- Weekly delivery sync — show progress, updates, and flagged risks
- Demo/Review at the end of each sprint or milestone

## Workflows
- Use the project board (e.g., GitHub Projects) with columns: Backlog, Ready, In Progress, In Review, QA, Done
- Pull Request workflow:
  - Small PRs (<= 400 lines when possible)
  - Include issue link and acceptance criteria in PR description
  - Run automated tests and linting in CI before requesting review
  - Require at least one approval before merging (or team-defined policy)

## Quality & Testing
- Unit tests for new logic
- Integration tests where applicable
- End-to-end smoke tests for critical flows before release
- Security scanning in CI
- Manual QA for feature acceptance when needed

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

## Blocker Escalation
- Level 1: Team-level triage in daily standup
- Level 2: PM escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

## Dependency Tracking & Bottleneck Reduction
Dependencies and bottlenecks can derail project timelines if not managed proactively.

### Identifying Dependencies
Dependencies fall into several categories:
- **Technical**: Shared libraries, APIs, infrastructure, platform features
- **Resource**: Availability of specific people, teams, or specialized skills
- **Business**: Approvals, contracts, partner commitments, regulatory requirements
- **Sequential**: Work that must be completed before other work can start

### Tracking Dependencies
- **Project Board**: Use a dedicated "Blocked" column or label
- **Dependency Log**: Maintain a simple table in the project README or tracking doc
  - Columns: ID, Description, Type, Blocking Item(s), Owner, Status, Target Resolution Date
- **Visual Indicators**: Use ⛔ emoji or red labels for blocked items
- **Cross-Team Dependencies**: Tag in GitHub issues and link related issues across repos

### Flagging Blocked Items
When work is blocked:
1. **Immediately** update the item status to "Blocked" with clear description
2. Add the blocker to the dependency log with owner and target resolution
3. **Raise in daily standup** for team awareness
4. **Escalate within 24 hours** if no clear path to resolution
5. Document any workarounds or parallel work that can proceed

### Who Owns Resolution
- **Technical blockers**: Engineering Lead or Tech Lead
- **Cross-team dependencies**: Project Manager coordinates with other PM
- **Business decisions**: Product Manager or Sponsor
- **Resource constraints**: Project Manager or Engineering Manager
- **Infrastructure**: Platform/DevOps team lead

### Reducing Bottlenecks
- **Work in parallel**: Identify tasks that can proceed independently
- **Create interfaces early**: Define API contracts so teams can work in parallel
- **Buffer critical path**: Add time buffers to tasks on the critical path
- **Cross-train**: Reduce single points of failure by knowledge sharing
- **Break down work**: Smaller tasks are easier to parallelize and less likely to block
- **Automate repetitive tasks**: Reduce manual bottlenecks in testing, deployment, reviews

### Dependency Escalation Documentation
When escalating a dependency:
1. **Document impact**: What's blocked, timeline risk, customer/business impact
2. **Propose solutions**: List 2-3 options with trade-offs
3. **Identify decision maker**: Who needs to approve the path forward
4. **Set deadline**: When do we need resolution to stay on track
5. **Follow up**: Track escalation in weekly status updates until resolved

## Execution Checklist
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] Regular demos scheduled
- [ ] Risk register updated weekly
- [ ] Dependency escalation process documented and communicated to team
- [ ] Blocked items clearly flagged with owners and target resolution dates
