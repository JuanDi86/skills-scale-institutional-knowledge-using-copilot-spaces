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
  - **Handoff to QA**: Move items to QA column after PR merge; include test plan and acceptance criteria in issue/story

## Role-Specific Handoffs

### Developer → QA Handoff
When moving work to QA:
- [ ] All acceptance criteria documented in the issue
- [ ] Test environment details provided (e.g., feature flag, staging URL)
- [ ] Known edge cases or test scenarios documented
- [ ] Demo or walkthrough available if needed
- [ ] Relevant documentation updated

### Developer → DevOps Handoff
When requiring infrastructure or deployment support:
- [ ] Infrastructure requirements documented (resources, configurations)
- [ ] Environment variables and secrets identified
- [ ] Deployment dependencies listed
- [ ] Rollback plan considered
- [ ] Monitoring and alerting requirements specified

## Quality & Testing
- Unit tests for new logic (owned by Developers)
- Integration tests where applicable (owned by Developers)
- End-to-end smoke tests for critical flows before release (coordinated with QA)
- Security scanning in CI (monitored by DevOps Engineer)
- Manual QA for feature acceptance when needed (owned by QA team)
- **QA Responsibilities**:
  - Validate acceptance criteria are met
  - Execute test plans and document results
  - Report bugs with clear reproduction steps
  - Sign off on features before release
  - Collaborate with UX Designer on usability validation

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

## Blocker Escalation
- Level 1: Team-level triage in daily standup
- Level 2: PM escalates to Product Lead and dependent teams
- Level 3: Sponsor-level escalation for business-impacting issues

## Execution Checklist
- [ ] Branching and PR conventions documented in repo (DevOps Engineer / Tech Lead)
- [ ] CI configured for tests and lint (DevOps Engineer)
- [ ] Regular demos scheduled (Project Manager)
- [ ] Risk register updated weekly (Project Manager)
- [ ] QA handoff process documented (Project Manager / QA Lead)
- [ ] Deployment process documented and tested (DevOps Engineer)
