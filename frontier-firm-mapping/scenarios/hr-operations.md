# 👥 HR Operations Transformation Scenario

> Empower employees with instant HR support while freeing HR teams for strategic work

---

## Overview

This scenario focuses on building an HR assistant agent that handles common employee inquiries about policies, benefits, time-off, and onboarding processes.

**Pattern:** HR Operations (Pattern 5)  
**Horizon:** H1-H2 (Individual Productivity to Workflow Automation)  
**Trust Level:** L1 → L2  
**Duration:** 1-2 days  
**Complexity:** Low-Medium

---

## Business Context

### The Challenge
- HR teams overwhelmed with repetitive questions
- Employees wait days for simple answers
- Policy information scattered across documents
- Inconsistent answers from different HR reps
- Onboarding process is manual and time-consuming

### The Solution
An HR assistant agent that:
- Answers policy questions instantly
- Guides employees through common processes
- Available 24/7 for global workforce
- Ensures consistent, accurate information
- Frees HR for strategic initiatives

---

## Objectives

By the end of this Agentathon, participants will have built:

- [ ] HR assistant agent in Copilot Studio
- [ ] Policy knowledge base integration
- [ ] Common HR process guidance (time-off, expenses, etc.)
- [ ] Escalation to HR team for complex cases
- [ ] Microsoft Teams deployment

---

## Prerequisites

### Technical Requirements
- Copilot Studio environment
- Microsoft Teams
- SharePoint (for policy documents)
- Optional: HR system access (Workday, SAP, etc.)

### Knowledge Base Preparation
- [ ] Employee handbook (PDF or web)
- [ ] Benefits summary documents
- [ ] Time-off policies
- [ ] Expense policy
- [ ] Onboarding checklist
- [ ] Organizational chart / contact directory

### Participant Preparation
- Review most common HR inquiries
- Identify top 10 time-consuming HR tasks
- Understand current HR tools and systems

---

## Agenda

### Option A: 1-Day Intensive

| Time | Activity |
|------|----------|
| 09:00 | Welcome, objectives, Copilot Studio overview |
| 10:00 | Use case prioritization workshop |
| 10:30 | ☕ Break |
| 10:45 | Agent design & knowledge base setup |
| 12:30 | 🍽️ Lunch |
| 13:30 | Hands-on building (core topics) |
| 15:30 | ☕ Break |
| 15:45 | Testing & refinement |
| 16:30 | Demo & next steps |
| 17:00 | Close |

### Option B: 2-Day Comprehensive

**Day 1:** Discovery, design, basic build  
**Day 2:** Advanced features, integrations, testing, demo

---

## Technical Implementation

### Agent Structure

```
HR Assistant Agent
├── System Topics
│   ├── Greeting
│   ├── Goodbye  
│   ├── Escalate (→ HR Team)
│   └── Fallback
│
├── Policy Topics
│   ├── Time Off & Leave
│   ├── Benefits Information
│   ├── Expense Policy
│   ├── Remote Work Policy
│   ├── Code of Conduct
│   └── General Policy Search
│
├── Process Guidance Topics
│   ├── Request Time Off
│   ├── Submit Expense Report
│   ├── Update Personal Information
│   ├── Enroll in Benefits
│   └── Report an Issue
│
├── Onboarding Topics
│   ├── New Employee Guide
│   ├── First Week Checklist
│   ├── IT Setup Help
│   └── Meet Your Team
│
├── Knowledge Sources
│   ├── Employee Handbook (SharePoint)
│   ├── Benefits Guide (PDF)
│   └── Policy Repository
│
└── Actions
    ├── Search Policies
    ├── Link to HR Portal
    └── Create HR Ticket (optional)
```

### Topics to Create

#### Topic 1: Time Off & Leave
```yaml
name: Time Off Information
trigger_phrases:
  - "How many vacation days do I have"
  - "Time off policy"
  - "Sick leave"
  - "Parental leave"
  - "How do I request PTO"
  - "Holiday schedule"

sub_intents:
  - vacation_balance: "Check my balance"
  - request_process: "How to request"
  - policy_details: "What's the policy"
  - types_of_leave: "What types exist"

conversation_flow:
  1. Identify specific question
  2. Search policy knowledge base
  3. Provide relevant information
  4. Offer to link to request system
  5. Ask if more help needed

sample_response: |
  📅 **Time Off Policy Summary**
  
  **Annual Leave:** 25 days per year (prorated for new joiners)
  **Sick Leave:** Up to 10 days per year
  **Personal Days:** 3 days per year
  
  **To request time off:**
  1. Go to [HR Portal](link)
  2. Select "Time Off Request"
  3. Choose dates and type
  4. Submit for manager approval
  
  Would you like me to explain any specific type of leave?
```

#### Topic 2: Benefits Information
```yaml
name: Benefits Information
trigger_phrases:
  - "What benefits do I have"
  - "Health insurance"
  - "Retirement plan"
  - "401k"
  - "Pension"
  - "Benefits enrollment"
  - "Dental coverage"

conversation_flow:
  1. Identify benefit type of interest
  2. Retrieve from benefits knowledge base
  3. Provide summary
  4. Offer detailed document link
  5. Suggest enrollment help if needed

trust_note: >
  Agent provides information only - does NOT make changes 
  to benefits enrollment. Always directs to official portal.
```

#### Topic 3: New Employee Onboarding
```yaml
name: New Employee Guide
trigger_phrases:
  - "I'm new here"
  - "First day"
  - "Onboarding"
  - "What do I need to do"
  - "Getting started"
  - "New employee"

conversation_flow:
  1. Welcome the new employee!
  2. Identify what they need help with
  3. Provide relevant checklist items
  4. Offer step-by-step guidance
  5. Connect to buddy/mentor if available

sample_response: |
  👋 **Welcome to the team!**
  
  Here's your first week checklist:
  
  ✅ **Day 1**
  - [ ] Complete IT setup (contact: it-support@company.com)
  - [ ] Review employee handbook
  - [ ] Set up direct deposit
  
  ✅ **Week 1**
  - [ ] Complete compliance training
  - [ ] Meet your team members
  - [ ] Schedule 1:1 with manager
  - [ ] Enroll in benefits (deadline: 30 days)
  
  What would you like help with first?
```

### Sample Conversations

**Conversation 1: Policy Question**
```
Employee: How many vacation days do I get?

Agent: Great question! Here's our vacation policy:
       
       📅 **Annual Vacation Allowance**
       
       Based on your tenure:
       • 0-2 years: 20 days
       • 3-5 years: 23 days  
       • 5+ years: 25 days
       
       Days reset on January 1st each year. 
       You can carry over up to 5 unused days.
       
       Would you like to know:
       • How to check your current balance?
       • How to request time off?
       • Our holiday schedule?

Employee: How do I check my balance?

Agent: To check your vacation balance:
       
       1. Log into [HR Portal](link)
       2. Click "My Time" 
       3. Select "Balances"
       
       You'll see all your leave types and remaining days.
       
       💡 Tip: You can also ask your manager to approve 
       time off directly in Microsoft Teams!
       
       Is there anything else I can help with?
```

**Conversation 2: Process Guidance**
```
Employee: I need to submit an expense report

Agent: I can help you with that! 
       
       💰 **Expense Report Process**
       
       **Step 1:** Gather your receipts
       - All expenses need receipts over €25
       - Take photos or scan to PDF
       
       **Step 2:** Submit via Expense System
       - Go to [Expense Portal](link)
       - Click "New Report"
       - Add each expense with receipt
       
       **Step 3:** Approval
       - Reports under €500: Manager approval
       - Reports over €500: Manager + Finance
       - Timeline: 3-5 business days
       
       **Important Policies:**
       • Meals: Max €50/day (domestic), €75/day (international)
       • Hotels: Must use preferred vendors
       • Flights: Economy class for trips under 6 hours
       
       Do you have questions about any specific expense type?
```

**Conversation 3: Escalation**
```
Employee: I have a complaint about my manager

Agent: I understand you want to discuss a concern about your manager. 
       This is important, and I want to make sure you get the right support.
       
       For sensitive matters like workplace concerns, it's best to 
       speak directly with HR.
       
       🔒 **Your options:**
       
       1. **HR Business Partner**
          Contact: [Name] - hr-partner@company.com
          
       2. **Employee Relations**
          Contact: employee-relations@company.com
          
       3. **Anonymous Hotline**
          Call: 1-800-XXX-XXXX
          
       All conversations are confidential.
       
       Would you like me to help you schedule a meeting with HR?
       
       [Escalated to: HR Team]
       [Reason: Employee relations concern]
       [Sensitivity: High - Manager complaint]
```

---

## Trust Configuration

### Initial Trust Level: L1-L2

```json
{
  "trust_config": {
    "level": 1.5,
    "name": "Information Provider",
    
    "capabilities": {
      "can_provide_information": true,
      "can_search_policies": true,
      "can_provide_links": true,
      "can_guide_processes": true,
      
      "cannot_modify_records": true,
      "cannot_approve_requests": true,
      "cannot_access_personal_data": true,
      "cannot_make_commitments": true
    },
    
    "escalation_required": [
      "salary_questions",
      "promotion_discussions", 
      "complaints_grievances",
      "termination_questions",
      "legal_matters",
      "harassment_reports",
      "accommodation_requests"
    ],
    
    "response_guidelines": {
      "always_cite_source": true,
      "include_disclaimer": "For official decisions, please consult HR directly.",
      "link_to_official_portal": true
    }
  }
}
```

### Important Trust Boundaries

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    HR AGENT TRUST BOUNDARIES                                │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  ✅ AGENT CAN:                     ❌ AGENT CANNOT:                         │
│  ═════════════                     ════════════════                         │
│  • Answer policy questions         • Access employee records                │
│  • Explain benefits               • Disclose salary information            │
│  • Guide through processes        • Approve/deny requests                  │
│  • Provide forms/links            • Make policy exceptions                 │
│  • Direct to right resources      • Discuss other employees                │
│  • Share public HR info           • Promise specific outcomes              │
│                                   • Handle complaints                       │
│                                   • Discuss performance                     │
│                                                                             │
│  ⚠️ ALWAYS ESCALATE:                                                       │
│  ══════════════════                                                         │
│  • Harassment or discrimination reports                                     │
│  • Workplace safety concerns                                                │
│  • Legal or compliance questions                                            │
│  • Requests for accommodation                                               │
│  • Salary and compensation questions                                        │
│  • Disciplinary matters                                                     │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Success Metrics

| Metric | Target | Measurement |
|--------|--------|-------------|
| Query Resolution Rate | 70% | Resolved without HR |
| Employee Satisfaction | 4.5/5 | Feedback survey |
| Response Time | <10 seconds | Automatic |
| HR Time Saved | 20 hours/week | Time tracking |
| Policy Accuracy | 100% | Audit review |
| Appropriate Escalations | 95% | Review sample |

---

## Post-Workshop Roadmap

### Phase 1: Policy Bot (Week 1-2)
- Deploy with policy Q&A only
- Gather feedback from pilot group
- Expand knowledge base

### Phase 2: Process Guide (Week 3-4)
- Add process guidance topics
- Link to HR systems
- Increase user base

### Phase 3: Proactive Support (Month 2)
- Onboarding automation
- Benefits enrollment reminders
- Training completion nudges

### Phase 4: Integration (Month 3+)
- Connect to HR systems (read-only)
- Personalized responses (balance, enrollment status)
- Advanced analytics

---

*This scenario is ideal for HR teams looking to provide better employee self-service while focusing on strategic HR initiatives.*
