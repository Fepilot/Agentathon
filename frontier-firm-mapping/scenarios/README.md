# 🎬 Agentathon Scenarios

> Complete end-to-end demonstration scenarios aligned with Frontier Firm patterns

---

## Overview

This folder contains detailed scenario playbooks for running themed Agentathons. Each scenario is designed as a complete 2-day workshop experience with all necessary materials.

---

## Available Scenarios

| Scenario | Pattern | Horizon | Complexity | Duration |
|----------|---------|---------|------------|----------|
| [Customer Service Excellence](./customer-service.md) | Customer Support | H2 | Medium | 2 days |
| [HR Operations Transformation](./hr-operations.md) | HR Operations | H1-H2 | Low-Medium | 1-2 days |
| [IT Service Desk Automation](./it-service-desk.md) | IT Service Management | H2 | Medium | 2 days |
| [Sales Enablement Agent](./sales-enablement.md) | Sales Enablement | H1-H2 | Medium | 2 days |
| [Back-Office Operations](./back-office.md) | Operations | H2-H3 | High | 2 days |

---

## Scenario Selection Guide

### For First-Time Agentathons
Start with **HR Operations** or **Customer Service** - these have:
- Clear, well-defined processes
- Readily available knowledge bases
- Lower risk for errors
- Quick wins to demonstrate value

### For Advanced Agentathons
Consider **IT Service Desk** or **Back-Office Operations** - these require:
- More complex integrations
- Multi-step workflows
- Higher trust level considerations
- More sophisticated orchestration

### Industry-Specific Recommendations

| Industry | Recommended First Scenario | Why |
|----------|---------------------------|-----|
| Banking | Customer Service | High volume, clear FAQs |
| Retail | Customer Service | Returns, order status |
| Manufacturing | IT Service Desk | Technical workforce |
| Healthcare | HR Operations | Policy-heavy environment |
| Professional Services | Sales Enablement | Client-facing value |

---

## Scenario Structure

Each scenario playbook includes:

```
scenario-name.md
├── Overview & Objectives
├── Prerequisites
├── Day 1 Agenda
│   ├── Morning: Discovery & Design
│   └── Afternoon: Initial Build
├── Day 2 Agenda
│   ├── Morning: Complete Build
│   └── Afternoon: Test & Demo
├── Technical Implementation
│   ├── Topics to Create
│   ├── Entities Required
│   ├── Actions/Connectors
│   └── Sample Conversations
├── Trust Configuration
├── Success Metrics
├── Common Challenges
└── Post-Workshop Roadmap
```

---

## Creating Custom Scenarios

Use this template to create new scenario playbooks:

```markdown
# [Scenario Name]

## Overview
Brief description of the scenario and business context.

## Objectives
By the end of this Agentathon, participants will have:
- [ ] Objective 1
- [ ] Objective 2
- [ ] Objective 3

## Prerequisites
- Technical requirements
- Knowledge base preparation
- Access requirements

## Frontier Firm Alignment
- **Pattern:** [Which of the 10 patterns]
- **Horizon:** [H1/H2/H3]
- **Trust Level:** [Starting level and graduation path]

## Agenda
### Day 1
[Detailed hour-by-hour agenda]

### Day 2
[Detailed hour-by-hour agenda]

## Technical Implementation
[Detailed technical guidance]

## Success Metrics
[How to measure success]

## Post-Workshop
[Production roadmap]
```

---

## Quick Reference: Pattern to Scenario Mapping

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    PATTERNS → SCENARIOS                                     │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  Pattern 1: Research & Analysis     →  Custom (Research Assistant)          │
│  Pattern 2: Software Development    →  Custom (DevOps scenario)             │
│  Pattern 3: Content Production      →  Marketing scenario (coming soon)     │
│  Pattern 4: Customer Support        →  customer-service.md ✅               │
│  Pattern 5: HR Operations           →  hr-operations.md ✅                  │
│  Pattern 6: Back-Office Operations  →  back-office.md ✅                    │
│  Pattern 7: IT Service Management   →  it-service-desk.md ✅                │
│  Pattern 8: Sales Enablement        →  sales-enablement.md ✅               │
│  Pattern 9: Supply Chain            →  Custom (industry-specific)           │
│  Pattern 10: Business Intelligence  →  Custom (BI scenario)                 │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

*Choose a scenario that matches your customer's industry and maturity level for the best Agentathon experience.*
