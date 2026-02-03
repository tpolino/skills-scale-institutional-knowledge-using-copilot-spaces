# OctoAcme — Cross-Functional Collaboration Guide

## Purpose
Ensure smooth handoffs and clear communication across roles during project execution, improving accountability and reducing coordination overhead.

## Principles
- Clear handoff criteria prevent rework and ambiguity
- Each role has defined "deliverables" that trigger the next phase
- Documentation and artifacts live in a single source of truth
- Communication happens asynchronously where possible, with synchronous touchpoints for complex decisions

---

## Key Collaboration Patterns

### 1. Product Manager → UX Designer

**When**: After problem statement is defined and user stories are prioritized

**Handoff Checklist**:
- [ ] User stories clearly define the problem to solve
- [ ] Success metrics and acceptance criteria are documented
- [ ] Target users or personas are identified
- [ ] Constraints or technical limitations are noted
- [ ] Timelines and design review dates are agreed upon

**Communication**:
- Kick-off meeting to align on problem space
- Async reviews via comments in design tools (Figma, etc.)
- Sync check-in midway through design phase

---

### 2. UX Designer → Developers

**When**: After designs are approved by Product Manager and ready for implementation

**Handoff Checklist**:
- [ ] Designs are finalized and linked in the user story or issue
- [ ] Interactive prototype demonstrates intended user flows
- [ ] Design specifications include dimensions, colors, spacing, and states (hover, active, disabled)
- [ ] Accessibility requirements are documented (color contrast, keyboard navigation, screen reader support)
- [ ] Edge cases and error states are designed
- [ ] Assets (icons, images) are exported and available

**Communication**:
- Design handoff session to walk through flows and clarify intent
- Availability for questions during implementation
- Review session before PR is merged to validate UI/UX implementation

---

### 3. Developers → QA/Testing

**When**: After feature implementation is complete and PR is ready for testing

**Handoff Checklist**:
- [ ] PR includes link to original issue with acceptance criteria
- [ ] Unit and integration tests pass in CI
- [ ] Manual testing instructions are provided if needed
- [ ] Known limitations or dependencies are documented
- [ ] Test environment or branch is specified
- [ ] Rollback plan is noted if applicable

**Communication**:
- PR description includes "How to Test" section
- QA provides feedback directly in PR comments
- Synchronous bug triage if critical issues are found

---

### 4. Developers → DevOps Engineer

**When**: Feature is ready for deployment or requires infrastructure changes

**Handoff Checklist**:
- [ ] Deployment requirements are documented (environment variables, config changes, database migrations)
- [ ] Dependencies on other services or APIs are identified
- [ ] Performance or scaling considerations are noted
- [ ] Monitoring and alerting needs are specified
- [ ] Rollback plan is documented
- [ ] Deployment window or timing constraints are communicated

**Communication**:
- Infrastructure change proposals submitted via issues or RFCs
- Sync review for complex deployments
- Post-deployment monitoring check-in

---

### 5. Scrum Master / Project Manager Coordination

**When**: Throughout project lifecycle to align on progress, risks, and blockers

**Collaboration Checklist**:
- [ ] Sprint goals and team capacity are aligned at planning
- [ ] Risks and dependencies are visible in project board and discussed weekly
- [ ] Blockers are escalated promptly if not resolved at team level
- [ ] Retrospective action items are tracked and completed
- [ ] Stakeholder communication is coordinated (PM handles external, Scrum Master focuses on team)

**Communication**:
- Daily standups facilitated by Scrum Master
- Weekly PM + Scrum Master sync to align on status and escalations
- Shared visibility into project boards and risk registers

---

## Role Handoff Matrix

Use this table to quickly identify what each role delivers to others:

| From Role | To Role | Key Deliverable(s) | Expected Outcome |
|-----------|---------|-------------------|------------------|
| Product Manager | UX Designer | User stories, success metrics, personas | Designs aligned to business goals |
| UX Designer | Developers | Wireframes, prototypes, design specs | Pixel-perfect, accessible UI |
| Developers | QA/Testing | PR with tests passing, testing instructions | Validated acceptance criteria |
| Developers | DevOps Engineer | Deployment requirements, runbooks | Reliable, automated deployments |
| QA/Testing | Product Manager | Test results, usability feedback | Confidence in release readiness |
| DevOps Engineer | Developers | Infrastructure access, CI/CD pipelines | Efficient, secure deployments |
| Scrum Master | Project Manager | Velocity data, team blockers | Informed project planning |
| Project Manager | All roles | Status updates, risk register, timelines | Alignment and transparency |

---

## Best Practices for Effective Collaboration

1. **Use Templates**: Standardize handoff artifacts (e.g., design handoff checklist, deployment checklist) to reduce missed steps
2. **Document Decisions**: Keep decisions in written form (GitHub discussions, decision logs) for reference and onboarding
3. **Assume Asynchronous First**: Write detailed context so teammates can contribute without requiring immediate responses
4. **Sync for Nuance**: Reserve meetings for complex problems, brainstorming, or alignment where real-time conversation adds value
5. **Close the Loop**: Confirm receipt and understanding of handoffs to avoid assumptions
6. **Surface Issues Early**: Don't wait for formal checkpoints—raise concerns as soon as they're identified

---

## When to Escalate

- **Level 1 (Team)**: Discuss in daily standup or tag relevant person in issue/PR
- **Level 2 (Project Manager / Scrum Master)**: Escalate if blocker persists >1 day or impacts sprint goals
- **Level 3 (Product Manager / Engineering Lead)**: Escalate if requires product decision, resource reallocation, or scope change
- **Level 4 (Sponsor)**: Escalate if business-critical risk or external dependency threatens delivery

---

## Using This Guide

- Reference this guide during sprint planning to align on handoff expectations
- Include relevant checklist sections in issue templates or project boards
- Review handoff quality in retrospectives and iterate on these practices
