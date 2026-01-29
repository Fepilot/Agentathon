# 🔍 Use Case Discovery Guide

Learn how to identify and define valuable use cases for AI agents.

---

## 🎯 Overview

Use case discovery is a critical first step in any Agentathon. This guide helps you identify high-value scenarios where AI agents can make a real impact.

---

## 🔎 Discovery Framework

### The 4 Questions

When evaluating potential use cases, ask:

1. **Frequency**: How often does this task occur?
2. **Volume**: How many people are affected?
3. **Complexity**: How difficult is the task?
4. **Value**: What's the business impact?

### Prioritization Matrix

| | Low Volume | High Volume |
|---|---|---|
| **High Value** | Consider | **Priority** |
| **Low Value** | Avoid | Consider |

---

## 📋 Discovery Workshop Template

### Part 1: Pain Point Identification (20 min)

Ask participants:

1. What questions do you answer repeatedly?
2. What information is hard to find?
3. What manual tasks take too much time?
4. Where do processes get stuck?

### Part 2: Categorization (15 min)

Group pain points by:

- **Department**: HR, IT, Sales, Finance, etc.
- **Task Type**: Information retrieval, process automation, decision support
- **User Type**: Internal employees, external customers, partners

### Part 3: Use Case Definition (25 min)

For each promising pain point, define:

```markdown
### Use Case: [Name]

**Description**: [What the agent will do]

**User**: [Who will use it]

**Trigger**: [How they'll invoke it]

**Expected Outcome**: [What success looks like]

**Data Sources**: [What information is needed]

**Actions**: [What the agent needs to do]
```

---

## 🏆 High-Value Use Case Patterns

### Pattern 1: Knowledge Agent

**Purpose**: Answer questions from organizational knowledge

**Examples**:
- HR Policy Assistant
- IT Support FAQ
- Product Information Bot

**Key Requirements**:
- Well-organized knowledge sources
- Clear, updated documentation
- Common questions identified

### Pattern 2: Process Assistant

**Purpose**: Guide users through complex processes

**Examples**:
- Expense Report Helper
- Onboarding Companion
- Leave Request Assistant

**Key Requirements**:
- Documented processes
- Clear decision points
- System integration (optional)

### Pattern 3: Data Retrieval Agent

**Purpose**: Fetch and present data from systems

**Examples**:
- Order Status Checker
- Project Dashboard Agent
- Inventory Lookup

**Key Requirements**:
- API or connector access
- Clear data structure
- User authentication (if needed)

### Pattern 4: Automation Agent

**Purpose**: Execute tasks on behalf of users

**Examples**:
- Meeting Scheduler
- Report Generator
- Notification Manager

**Key Requirements**:
- Power Automate integration
- Clear trigger conditions
- Approval workflows (if needed)

---

## 📝 Use Case Template

Use this template to document your use cases:

```markdown
# Use Case: [Name]

## Overview
| Field | Value |
|-------|-------|
| **Owner** | [Name] |
| **Department** | [Department] |
| **Priority** | High / Medium / Low |
| **Complexity** | Simple / Medium / Complex |

## Description
[2-3 sentences describing the use case]

## Current State
[How is this handled today?]

## Target State
[How will the AI agent improve this?]

## Users
- Primary: [Who uses it most]
- Secondary: [Other users]

## Trigger Scenarios
1. [When user needs X...]
2. [When user asks about Y...]

## Knowledge Sources
- [ ] [Source 1]
- [ ] [Source 2]

## Actions Required
- [ ] [Action 1]
- [ ] [Action 2]

## Success Metrics
- [ ] [Metric 1]
- [ ] [Metric 2]

## Risks & Considerations
- [Risk 1]
- [Risk 2]
```

---

## 🚫 Anti-Patterns to Avoid

### Don't Build Agents For:

1. **Highly sensitive decisions**: Hiring, firing, legal judgments
2. **Rare edge cases**: Low volume, high complexity
3. **Undocumented processes**: No source of truth
4. **Rapidly changing information**: Without update mechanisms
5. **Tasks requiring empathy**: Grief counseling, conflict resolution

---

## ✅ Use Case Readiness Checklist

Before building, ensure:

- [ ] Clear problem statement defined
- [ ] Target users identified
- [ ] Knowledge sources available
- [ ] Success metrics established
- [ ] Stakeholder buy-in obtained
- [ ] Technical feasibility confirmed

---

## 📊 Example Use Cases by Industry

### Banking / Financial Services
- Account information assistant
- Loan application guide
- Investment FAQ bot
- Compliance helper

### Retail
- Product recommendation agent
- Order tracking assistant
- Returns process guide
- Inventory checker

### Healthcare
- Appointment scheduler
- Symptom checker (non-diagnostic)
- Patient FAQ assistant
- Staff onboarding helper

### Manufacturing
- Equipment maintenance guide
- Safety procedure assistant
- Inventory management agent
- Quality control helper

---

## 🎯 Agentathon Use Case Selection

For your Agentathon, select use cases that are:

- ✅ Achievable in 1-2 days
- ✅ Have available knowledge sources
- ✅ Provide clear value demonstration
- ✅ Don't require complex integrations (for Day 1)
- ✅ Representative of real business needs
