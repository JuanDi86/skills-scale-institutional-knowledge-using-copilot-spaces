# OctoAcme Project Management Guide

Welcome to the OctoAcme project management documentation! This guide provides an overview of how we run projects at OctoAcme, from initial concept through successful delivery and continuous improvement.

## Overview

OctoAcme follows an **iterative, customer-first approach** to project delivery. We emphasize clear ownership, data-informed decisions, and psychological safety across all project phases. Our processes are designed to deliver small, testable increments while maintaining high quality standards and transparent communication.

### Core Principles

- **Customer-first**: Prioritize customer value and usability
- **Iterative delivery**: Deliver small, testable increments
- **Clear ownership**: Each project has a named Project Manager (PM) and Product Manager (PdM, also called "Product Lead")
- **Data-informed decisions**: Measure impact and iterate based on evidence
- **Psychological safety**: Encourage feedback and learning

## Project Lifecycle

Our projects follow a structured lifecycle with five key phases:

1. **Initiation** → Define problem statement, stakeholders, and high-level timeline
2. **Planning** → Break down scope, estimate resources, identify dependencies and milestones
3. **Execution** → Build, test, review, and iterate on deliverables
4. **Release** → Deploy to production, verify functionality, and announce to stakeholders
5. **Close & Retrospective** → Capture learnings and convert them into actionable improvements

## Key Workflows

### Project One-Pager
Every project starts with a concise one-pager that defines the problem, objectives, success metrics, stakeholders, timeline, and initial risks. This artifact ensures alignment before committing significant resources.

### Planning & Kickoff
Planning transforms approved initiatives into actionable plans with:
- Prioritized backlog with acceptance criteria
- Definition of Done (DoD)
- Release timeline and milestone mapping
- Risk and dependency identification

### Backlog Management & Acceptance Criteria
Work items include clear acceptance criteria, priorities, estimates, and ownership. Items must meet the DoD before being considered complete.

### GitHub Project Board Workflow
We use GitHub Projects to track work through these stages:
- **Backlog** → **Ready** → **In Progress** → **In Review** → **QA** → **Done**

### Pull Request (PR) Workflow
- Keep PRs small (≤400 lines when possible)
- Link to related issues and include acceptance criteria in PR description
- Run automated tests and linting in CI before requesting review
- Require at least one approval before merging
- Address code review feedback promptly

### Risk Register & Escalation
Risks are tracked with impact, likelihood, owner, and mitigation plans. Escalation paths:
- **Level 1**: Team-level triage in daily standup
- **Level 2**: PM escalates to Product Lead and dependent teams
- **Level 3**: Sponsor-level escalation for business-impacting issues

### Release & Deployment Checklist
Pre-release requirements include:
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted
- Rollback/mitigation plan documented
- Smoke tests prepared

Deployment follows a structured checklist including staging verification, production deployment, post-deploy checks, and stakeholder announcements.

### Retrospectives & Action Items
After each sprint, release, or milestone, we conduct retrospectives to identify what went well and what could be improved. Action items are tracked in the project backlog with clear owners and timelines.

## Roles & Personas

### Project Manager (PM)
Coordinates delivery activities, manages schedules, risks, and communications. Facilitates meetings and ensures transparency across stakeholders.

### Product Manager (PdM)
Defines what should be built to deliver customer and business value. Owns product vision, prioritizes the backlog, and measures outcomes.

### Developers
Design, build, test, and deliver software components. Write tests, participate in code reviews, and help identify technical risks.

### QA/Testing
Validate quality and acceptance criteria through manual and automated testing approaches.

### Stakeholders
Provide inputs, approvals, and feedback throughout the project lifecycle.

## Communication Strategies

### Regular Cadence
- **Daily standups** (15 min) — Progress, blockers, dependencies
- **Weekly delivery sync** — Progress updates and flagged risks
- **Demo/Review** — At the end of each sprint or milestone
- **Weekly PM + PdM sync** — Alignment on priorities and decisions
- **Monthly stakeholder updates** — High-level progress and key decisions

### Single Source of Truth
Project status, documentation, and decisions are maintained in the project repository and GitHub Project board to ensure all stakeholders have access to current information.

### Escalation Paths
Clear escalation paths ensure blockers and issues are addressed promptly:
- Team-level → PM → Product Lead → Sponsor
- Security incidents follow the security incident runbook

### Communication Templates
We use standardized templates for weekly status updates and incident communication to ensure consistency and completeness.

## Quality Assurance

Our quality practices ensure reliable, secure deliverables:

### Testing Strategy
- **Unit tests** for new logic and business rules
- **Integration tests** for component interactions
- **End-to-end (E2E) smoke tests** for critical user flows before release
- **Manual QA** for feature acceptance when automated testing is insufficient

### Security Scanning
All code changes undergo security scanning in CI to identify vulnerabilities early in the development process.

### CI Gates
Continuous Integration (CI) runs automated tests, linting, and security scans on every PR. All checks must pass before code can be merged.

### Code Review
At least one approval is required for all PRs. Reviews focus on correctness, maintainability, security, and adherence to coding standards.

## Documentation Index

Explore our detailed process documentation:

- **[Project Management Overview](octoacme-project-management-overview.md)** — Principles, roles, and artifacts
- **[Roles & Personas](octoacme-roles-and-personas.md)** — Detailed role definitions and responsibilities
- **[Project Initiation](octoacme-project-initiation.md)** — One-pager template and initiation checklist
- **[Project Planning](octoacme-project-planning.md)** — Backlog creation, estimation, and sprint planning
- **[Execution & Tracking](octoacme-execution-and-tracking.md)** — Daily workflows, PR process, and quality practices
- **[Risk Management & Communication](octoacme-risks-and-communication.md)** — Risk register, stakeholder communication, and escalation
- **[Release & Deployment](octoacme-release-and-deployment.md)** — Deployment checklist and rollback procedures
- **[Retrospective & Continuous Improvement](octoacme-retrospective-and-continuous-improvement.md)** — Learning capture and action tracking

## Getting Started

**New to OctoAcme projects?** Follow this onboarding path:

1. Start with the **[Project Management Overview](octoacme-project-management-overview.md)** for foundational concepts
2. Review **[Roles & Personas](octoacme-roles-and-personas.md)** to understand your role and how you interact with others
3. Walk through the lifecycle docs in order: Initiation → Planning → Execution → Release → Retrospective
4. Bookmark **[Execution & Tracking](octoacme-execution-and-tracking.md)** for daily reference on PR workflows and quality practices
5. Keep **[Risk Management & Communication](octoacme-risks-and-communication.md)** handy for escalation paths and communication templates

## Questions or Feedback?

If you have questions about these processes or suggestions for improvement, reach out to your Project Manager or Product Manager (PdM). We continuously refine our practices based on team feedback and retrospective insights.
