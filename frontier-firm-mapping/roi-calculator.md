# 📈 ROI Calculator & Measurement Framework

> Quantifying the business value of AI agents built during Agentathons

---

## Overview

Measuring ROI is critical for justifying AI agent investments and planning production deployments. This guide provides templates and methodologies for calculating and tracking the business impact of agents built during Agentathons.

---

## The ROI Framework

### Core Metrics

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                         ROI METRICS FRAMEWORK                               │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│   EFFICIENCY METRICS              │   QUALITY METRICS                       │
│   ══════════════════              │   ═══════════════                       │
│   • Time saved per task           │   • Error reduction rate                │
│   • Tasks automated per day       │   • First-contact resolution           │
│   • Automation rate (%)           │   • Accuracy score                     │
│   • Processing speed              │   • Compliance rate                    │
│                                                                             │
│   SATISFACTION METRICS            │   FINANCIAL METRICS                    │
│   ════════════════════            │   ═════════════════                    │
│   • User satisfaction (NPS)       │   • Cost per transaction               │
│   • Employee satisfaction         │   • Revenue impact                     │
│   • Customer satisfaction         │   • Cost avoidance                     │
│   • Adoption rate                 │   • Productivity gains                 │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Pre-Agentathon: Baseline Measurement

Before the Agentathon, capture these baseline metrics for target use cases:

### Baseline Data Collection Template

```markdown
## Use Case Baseline Assessment

**Use Case:** _________________________________
**Date:** _________________________________
**Assessed By:** _________________________________

### Volume Metrics
- Average tasks per day: _______
- Average tasks per week: _______
- Average tasks per month: _______
- Peak volume periods: _______

### Time Metrics
- Average handling time per task: _______ minutes
- Total time spent per day: _______ hours
- Total time spent per month: _______ hours

### Quality Metrics
- Current error rate: _______ %
- Rework rate: _______ %
- Escalation rate: _______ %
- Customer satisfaction: _______ /5

### Cost Metrics
- Hourly cost of employee: € _______
- Monthly cost for this process: € _______
- Annual cost for this process: € _______

### Pain Points
1. _________________________________
2. _________________________________
3. _________________________________
```

---

## ROI Calculation Templates

### Template 1: Time Savings ROI

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                    TIME SAVINGS CALCULATION                                 │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  INPUTS                                                                     │
│  ══════                                                                     │
│  A. Tasks per month:                    ____________                        │
│  B. Current time per task (minutes):    ____________                        │
│  C. Expected automation rate (%):       ____________                        │
│  D. Time reduction for automated (%):   ____________                        │
│  E. Hourly labor cost (€):              ____________                        │
│                                                                             │
│  CALCULATIONS                                                               │
│  ════════════                                                               │
│  F. Current monthly hours = (A × B) / 60                                    │
│     = ____________ hours/month                                              │
│                                                                             │
│  G. Tasks automated = A × (C / 100)                                         │
│     = ____________ tasks/month                                              │
│                                                                             │
│  H. Hours saved = G × B × (D / 100) / 60                                    │
│     = ____________ hours/month                                              │
│                                                                             │
│  I. Monthly savings = H × E                                                 │
│     = € ____________ /month                                                 │
│                                                                             │
│  J. Annual savings = I × 12                                                 │
│     = € ____________ /year                                                  │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Template 2: Full ROI Calculation

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                       FULL ROI CALCULATION                                  │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  COSTS (Year 1)                                                             │
│  ══════════════                                                             │
│  Copilot Studio licenses:           € ____________                          │
│  Development time (Agentathon):     € ____________                          │
│  Post-workshop refinement:          € ____________                          │
│  Training & change management:      € ____________                          │
│  Ongoing maintenance (annual):      € ____________                          │
│  ─────────────────────────────────────────────────                          │
│  TOTAL COST (Year 1):               € ____________                          │
│                                                                             │
│  BENEFITS (Year 1)                                                          │
│  ═════════════════                                                          │
│  Time savings (from Template 1):    € ____________                          │
│  Error reduction savings:           € ____________                          │
│  Faster resolution value:           € ____________                          │
│  Employee satisfaction gains:       € ____________                          │
│  Customer satisfaction impact:      € ____________                          │
│  ─────────────────────────────────────────────────                          │
│  TOTAL BENEFITS (Year 1):           € ____________                          │
│                                                                             │
│  ROI METRICS                                                                │
│  ═══════════                                                                │
│  Net Benefit = Benefits - Costs:    € ____________                          │
│  ROI % = (Net Benefit / Costs) × 100: ____________ %                        │
│  Payback Period (months):           ____________                            │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Sample ROI Scenarios

### Scenario A: Customer Service Agent

```
┌─────────────────────────────────────────────────────────────────────────────┐
│              CUSTOMER SERVICE AGENT ROI EXAMPLE                             │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  BASELINE                                                                   │
│  • 2,000 customer inquiries per month                                       │
│  • 12 minutes average handling time                                         │
│  • 400 hours/month total agent time                                         │
│  • €35/hour fully loaded cost                                               │
│  • €14,000/month labor cost                                                 │
│                                                                             │
│  WITH AI AGENT                                                              │
│  • 50% deflection rate (1,000 inquiries handled by AI)                      │
│  • Remaining 1,000 inquiries: 8 min avg (AI assists human)                  │
│  • AI-handled: 0 human hours                                                │
│  • Human-handled: 133 hours/month                                           │
│  • New labor cost: €4,667/month                                             │
│                                                                             │
│  SAVINGS                                                                    │
│  • Monthly savings: €14,000 - €4,667 = €9,333                               │
│  • Annual savings: €112,000                                                 │
│                                                                             │
│  COSTS                                                                      │
│  • Copilot Studio (10 users): €2,400/year                                   │
│  • Development (Agentathon + refinement): €8,000                            │
│  • Training: €2,000                                                         │
│  • Maintenance: €3,000/year                                                 │
│  • Total Year 1: €15,400                                                    │
│                                                                             │
│  ROI                                                                        │
│  • Net Benefit Year 1: €112,000 - €15,400 = €96,600                         │
│  • ROI: 627%                                                                │
│  • Payback: 1.6 months                                                      │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Scenario B: HR Operations Agent

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                  HR OPERATIONS AGENT ROI EXAMPLE                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  BASELINE                                                                   │
│  • 500 HR inquiries per month                                               │
│  • 15 minutes average response time                                         │
│  • 125 hours/month HR team time                                             │
│  • €45/hour HR specialist cost                                              │
│  • €5,625/month labor cost                                                  │
│                                                                             │
│  WITH AI AGENT                                                              │
│  • 70% handled by AI (policy questions, benefits info)                      │
│  • 30% escalated to HR (complex cases)                                      │
│  • Escalated cases: 10 min avg (AI provides context)                        │
│  • New HR time: 25 hours/month                                              │
│  • New labor cost: €1,125/month                                             │
│                                                                             │
│  ADDITIONAL BENEFITS                                                        │
│  • 24/7 availability (previously 9-5 only)                                  │
│  • Consistent answers (policy compliance)                                   │
│  • Employee satisfaction improvement                                        │
│                                                                             │
│  SAVINGS                                                                    │
│  • Monthly savings: €4,500                                                  │
│  • Annual savings: €54,000                                                  │
│  • Plus: HR team can focus on strategic work                                │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Scenario C: IT Support Agent

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                   IT SUPPORT AGENT ROI EXAMPLE                              │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  BASELINE                                                                   │
│  • 800 IT tickets per month                                                 │
│  • 25 minutes average resolution time                                       │
│  • 333 hours/month support time                                             │
│  • €40/hour IT support cost                                                 │
│  • €13,333/month labor cost                                                 │
│                                                                             │
│  WITH AI AGENT                                                              │
│  • 40% auto-resolved (password resets, common issues)                       │
│  • 35% guided resolution (agent helps user self-serve)                      │
│  • 25% escalated to IT team                                                 │
│  • New IT time: 100 hours/month                                             │
│  • New labor cost: €4,000/month                                             │
│                                                                             │
│  ADDITIONAL BENEFITS                                                        │
│  • Faster resolution (immediate vs. ticket queue)                           │
│  • Reduced employee downtime                                                │
│  • Better documentation of issues                                           │
│                                                                             │
│  SAVINGS                                                                    │
│  • Monthly savings: €9,333                                                  │
│  • Annual savings: €112,000                                                 │
│  • Employee productivity gain: ~2,000 hours/year                            │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Tracking Dashboard

### Key Metrics to Monitor

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                      AGENT ROI DASHBOARD                                    │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  📊 EFFICIENCY                    📈 QUALITY                                │
│  ═════════════                    ══════════                                │
│  Automation Rate:    [====----]   Accuracy:         [========--]            │
│  Currently: 52%      Target: 70%  Currently: 94%    Target: 95%             │
│                                                                             │
│  Resolution Time:    [======--]   User Satisfaction: [========-]            │
│  Currently: 3.2 min  Target: 2m   Currently: 4.6/5   Target: 4.5            │
│                                                                             │
│  💰 FINANCIAL                     📅 TIMELINE                               │
│  ═══════════                      ════════════                              │
│  Monthly Savings:    €8,450       Deployed: 45 days ago                     │
│  Annual Projection:  €101,400     ROI Break-even: ✅ Achieved               │
│  ROI to Date:        312%         Next Review: Feb 15                       │
│                                                                             │
│  📉 TREND (Last 30 Days)                                                    │
│  ════════════════════════                                                   │
│  [Line graph showing improvement in key metrics over time]                  │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Monthly ROI Report Template

```markdown
# Monthly Agent ROI Report

**Agent:** Customer Service Agent
**Period:** January 2026
**Report Date:** February 1, 2026

## Executive Summary
The agent handled 1,050 interactions this month with a 94% success rate,
generating estimated savings of €9,200.

## Key Metrics

| Metric | Target | Actual | Status |
|--------|--------|--------|--------|
| Automation Rate | 50% | 52% | ✅ |
| Accuracy | 95% | 94% | ⚠️ |
| User Satisfaction | 4.5 | 4.6 | ✅ |
| Monthly Savings | €8,000 | €9,200 | ✅ |

## Volume Analysis
- Total interactions: 1,050
- Handled by agent: 546 (52%)
- Escalated to human: 504 (48%)

## Quality Analysis
- Correct resolutions: 513/546 (94%)
- Errors identified: 33
- Error categories:
  - Misunderstood intent: 18
  - Outdated information: 10
  - Technical issues: 5

## Recommendations
1. Update knowledge base for [topic] - should improve accuracy by ~2%
2. Add new intent for [common question pattern]
3. Consider increasing trust level based on performance

## Next Month Targets
- Automation rate: 55%
- Accuracy: 96%
- Monthly savings: €10,000
```

---

## ROI Presentation for Stakeholders

### Slide 1: The Opportunity

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                                                                             │
│   💡 THE OPPORTUNITY                                                        │
│                                                                             │
│   Current State:                                                            │
│   • 2,000 inquiries/month handled manually                                  │
│   • €14,000/month in labor costs                                            │
│   • 12 minute average response time                                         │
│   • Limited to business hours                                               │
│                                                                             │
│   With AI Agent:                                                            │
│   • 50% automation potential                                                │
│   • €112,000 annual savings                                                 │
│   • <2 minute response time                                                 │
│   • 24/7 availability                                                       │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Slide 2: The Investment

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                                                                             │
│   💰 THE INVESTMENT                                                         │
│                                                                             │
│   One-Time Costs:                                                           │
│   ├── Agentathon workshop:      €5,000                                      │
│   ├── Post-workshop refinement: €3,000                                      │
│   └── Training & adoption:      €2,000                                      │
│       Subtotal:                 €10,000                                     │
│                                                                             │
│   Annual Costs:                                                             │
│   ├── Copilot Studio licenses:  €2,400                                      │
│   └── Maintenance & updates:    €3,000                                      │
│       Subtotal:                 €5,400                                      │
│                                                                             │
│   Total Year 1:                 €15,400                                     │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Slide 3: The Return

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                                                                             │
│   📈 THE RETURN                                                             │
│                                                                             │
│   Year 1:                                                                   │
│   • Gross savings:      €112,000                                            │
│   • Investment:         €15,400                                             │
│   • Net benefit:        €96,600                                             │
│   • ROI:                627%                                                │
│   • Payback period:     1.6 months                                          │
│                                                                             │
│   Year 2+:                                                                  │
│   • Gross savings:      €112,000                                            │
│   • Investment:         €5,400                                              │
│   • Net benefit:        €106,600                                            │
│   • ROI:                1,974%                                              │
│                                                                             │
│   3-Year Total Net Benefit: €309,800                                        │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

## Quick ROI Estimator

Use this quick estimator during Agentathon discovery sessions:

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                      QUICK ROI ESTIMATOR                                    │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│  Step 1: Volume                                                             │
│  Tasks per month: _______ × 12 = _______ tasks/year                         │
│                                                                             │
│  Step 2: Time                                                               │
│  Minutes per task: _______ ÷ 60 = _______ hours/task                        │
│  Total hours/year: _______ (tasks) × _______ (hours) = _______              │
│                                                                             │
│  Step 3: Cost                                                               │
│  Hourly rate: € _______                                                     │
│  Annual cost: _______ hours × € _______ = € _______                         │
│                                                                             │
│  Step 4: Savings (assume 50% automation)                                    │
│  Potential annual savings: € _______ × 0.5 = € _______                      │
│                                                                             │
│  Step 5: Quick ROI                                                          │
│  Investment (estimate €15,000 Year 1): € 15,000                             │
│  Net benefit: € _______ - €15,000 = € _______                               │
│  Quick ROI: Worth pursuing? [ ] Yes [ ] Maybe [ ] No                        │
│                                                                             │
└─────────────────────────────────────────────────────────────────────────────┘
```

---

*This ROI framework helps justify AI agent investments and track ongoing value delivery.*
