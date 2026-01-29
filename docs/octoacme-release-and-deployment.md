# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged (verified by Product Manager / Project Manager)
- Passing CI and security scans (verified by DevOps Engineer)
- Release notes drafted (owned by Product Manager with input from Developers)
- Rollback / mitigation plan documented (owned by DevOps Engineer)
- Smoke tests prepared (coordinated between QA and DevOps Engineer)
- **DevOps Sign-off**: Infrastructure and deployment readiness confirmed

## Deployment Checklist
- [ ] Deployment window scheduled (if needed) — Project Manager coordinates
- [ ] Backup or snapshot (if applicable) — DevOps Engineer executes
- [ ] Deploy to staging and run smoke tests — DevOps Engineer and QA collaborate
- [ ] Deploy to production (automated pipeline preferred) — DevOps Engineer executes
- [ ] Run post-deploy verifications — DevOps Engineer with QA support
- [ ] Announce release to stakeholders and support — Product Manager / Project Manager
- [ ] Monitor metrics and error rates — DevOps Engineer and Data Analyst

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call (DevOps Engineer leads)
  - Rollback to last known-good release if necessary (DevOps Engineer executes)
  - Triage root cause and capture action items (cross-functional team)

## Release Coordination & Handoffs

### Product Manager → DevOps Engineer Handoff
Before release:
- [ ] Release scope and timeline communicated
- [ ] Success metrics and monitoring requirements defined
- [ ] Stakeholder communication plan agreed
- [ ] Go/no-go criteria established

### QA → DevOps Engineer Handoff
Before production deployment:
- [ ] Staging environment tests passed
- [ ] Critical flows validated
- [ ] Known issues documented and risk-assessed
- [ ] Smoke test checklist provided for post-deploy verification

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
