# OctoAcme — Risk Management & Communication

## Purpose
Explain how to identify, manage, and communicate risks and dependencies.

## Risk Register
Maintain a simple table with:
- ID
- Description
- Impact (High/Med/Low)
- Likelihood (High/Med/Low)
- Owner
- Mitigation plan
- Status

### Example Risk Register
Below is an example risk register for reference. Maintain your project's risk register in the project repo README or dedicated tracking document.

| ID | Description | Impact | Likelihood | Owner | Mitigation Plan | Status |
|----|-------------|--------|------------|-------|-----------------|--------|
| R1 | Third-party API rate limits may block production traffic | High | Medium | Engineering Lead | Implement caching layer, request queuing, and fallback mechanism | Active |
| R2 | Key developer unavailable during critical sprint | Medium | Low | PM | Cross-train 2 team members on critical components, document architecture | Mitigated |
| R3 | Regulatory approval delay could push launch by 4 weeks | High | Medium | Product Manager | Start compliance review early, maintain weekly contact with legal | Active |
| R4 | Database migration may cause downtime >4 hours | High | Low | DevOps Lead | Practice migration in staging, prepare rollback scripts, schedule maintenance window | Mitigated |
| R5 | Unclear requirements from stakeholder group | Medium | Medium | PM | Schedule requirements workshop, create prototype for validation | Closed |

### Risk Status Definitions
- **Active**: Risk is present and being monitored; mitigation plan in progress
- **Mitigated**: Mitigation plan implemented; risk reduced to acceptable level
- **Closed**: Risk no longer applies or has been fully addressed
- **Realized**: Risk has occurred; now an issue being tracked separately

## Risk Lifecycle
- Identify: during planning and ongoing execution
- Assess: estimate impact and likelihood
- Mitigate: reduced via actions, contingency plans
- Monitor: review at weekly syncs and update status

## Stakeholder Communication
- Identify stakeholder groups and communication needs (e.g., engineering, sales, support)
- Provide regular updates (weekly or milestone-based)
- Use a single source of truth (project README or release doc) for status

### Stakeholder Update Frequency & Visibility
Clear, consistent stakeholder communication builds trust and ensures alignment.

**Stakeholder Communication Checklist:**
- [ ] Stakeholder groups identified and documented (engineering, leadership, customers, support, etc.)
- [ ] Update frequency defined for each group (daily, weekly, milestone-based, etc.)
- [ ] Communication channels established (email, Slack, status dashboard, etc.)
- [ ] Single source of truth designated for project status (README, wiki, or project board)
- [ ] Top risks and mitigation plans visible to stakeholders
- [ ] Escalation paths documented and communicated
- [ ] Feedback mechanisms in place for stakeholders to ask questions or raise concerns

**Recommended Update Cadence by Stakeholder Group:**
- **Core Team**: Daily standups, real-time Slack updates
- **Extended Team** (adjacent teams, SMEs): Weekly async updates or milestone-based
- **Leadership**: Bi-weekly or monthly summaries with key metrics and top risks
- **Customers/End Users**: Major milestone announcements, release notes, opt-in beta updates
- **Support/Operations**: Pre-release briefings, runbook updates, post-release check-ins

**Visibility on Top Risks:**
- Include top 3-5 risks in weekly stakeholder updates
- Use simple Red/Yellow/Green status indicators
- Provide brief mitigation status and any help needed
- Escalate risks trending worse or requiring stakeholder decisions

## Communication Templates
Weekly Status Template:
- Progress this week:
- Next steps:
- Risks & blockers:
- Ask / decisions needed:

Incident Communication
- Triage summary
- Actions being taken
- Expected timeline
- Post-incident blameless retrospective scheduled

## Escalation Paths
- Team-level -> PM -> Product Lead -> Sponsor
- For security incidents, follow the security incident runbook and notify Security on-call
