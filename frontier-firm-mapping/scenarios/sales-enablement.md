# 📈 Sales Enablement Agent Scenario

> Empower sales teams with instant access to information, proposals, and customer insights

---

## Overview

This scenario focuses on building a sales assistant agent that helps sales representatives with product information, proposal generation, and CRM updates.

**Pattern:** Sales Enablement (Pattern 8)  
**Horizon:** H1-H2 (Individual Productivity to Workflow Automation)  
**Trust Level:** L1 → L2  
**Duration:** 2 days  
**Complexity:** Medium

---

## Business Context

### The Challenge
- Sales reps spend 30% of time on administrative tasks
- Product information scattered across multiple sources
- Proposal creation is time-consuming
- CRM data entry often neglected
- Slow response to customer inquiries

### The Solution
A sales assistant agent that:
- Provides instant product and pricing information
- Assists with proposal drafting
- Updates CRM automatically
- Surfaces relevant customer insights
- Prepares meeting briefs

---

## Objectives

By the end of this Agentathon, participants will have built:

- [ ] Sales assistant agent in Copilot Studio
- [ ] Product knowledge base integration
- [ ] Proposal draft generator
- [ ] CRM integration (read + suggest updates)
- [ ] Meeting preparation assistant

---

## Technical Implementation

### Agent Structure

```
Sales Assistant Agent
├── System Topics
│   ├── Greeting
│   ├── Goodbye
│   └── Fallback
│
├── Information Topics
│   ├── Product Information
│   ├── Pricing Details
│   ├── Competitive Comparison
│   ├── Case Studies
│   └── Discount Policies
│
├── Productivity Topics
│   ├── Draft Proposal
│   ├── Meeting Prep Brief
│   ├── Follow-up Email Draft
│   ├── Update Opportunity
│   └── Log Activity
│
├── Insights Topics
│   ├── Customer Summary
│   ├── Opportunity Status
│   ├── Recent Interactions
│   └── Renewal Alerts
│
├── Knowledge Sources
│   ├── Product Catalog
│   ├── Price List
│   ├── Competitor Analysis
│   ├── Case Study Library
│   └── Sales Playbooks
│
└── Actions
    ├── Search Products
    ├── Get Customer Data (CRM)
    ├── Draft Document
    ├── Update CRM (with approval)
    └── Schedule Meeting
```

### Key Topics

#### Topic 1: Product Information
```yaml
name: Product Information
trigger_phrases:
  - "Tell me about [product]"
  - "Product features"
  - "What does [product] do"
  - "Compare products"
  - "Product pricing"

conversation_flow:
  1. Identify product of interest
  2. Search product knowledge base
  3. Present relevant information
  4. Offer pricing details
  5. Suggest related case studies
```

#### Topic 2: Draft Proposal
```yaml
name: Draft Proposal
trigger_phrases:
  - "Create a proposal"
  - "Draft proposal for"
  - "Need a proposal"
  - "Proposal template"

trust_level: L2 (draft only, human reviews)

conversation_flow:
  1. Get customer name and context
  2. Pull customer data from CRM
  3. Identify products/services needed
  4. Generate proposal draft
  5. Present for review and editing
```

#### Topic 3: Meeting Prep
```yaml
name: Meeting Preparation
trigger_phrases:
  - "Prepare me for my meeting with"
  - "Meeting brief"
  - "What should I know about"
  - "Customer background"

conversation_flow:
  1. Identify customer
  2. Pull recent interactions from CRM
  3. Summarize open opportunities
  4. Note recent support tickets
  5. Suggest talking points
```

### Sample Conversations

**Conversation 1: Meeting Prep**
```
Sales Rep: Prepare me for my meeting with Acme Corp tomorrow

Agent: 📋 **Meeting Brief: Acme Corp**
       
       **Company Overview**
       • Industry: Manufacturing
       • Size: 500 employees
       • Current Customer: Yes (since 2023)
       • Account Owner: You (Sarah Johnson)
       
       **Current Relationship**
       • Products: Basic Plan ($2,400/year)
       • Contract Renewal: March 2026 (47 days away)
       • Health Score: 🟡 Medium (72/100)
       
       **Recent Activity**
       • Jan 28: Support ticket about integration (resolved)
       • Jan 15: Usage report sent
       • Dec 10: QBR conducted
       
       **Open Opportunities**
       • Upgrade to Pro Plan - Stage: Proposal - $8,500
       • Add-on Module - Stage: Discovery - $2,000
       
       **Suggested Talking Points**
       1. Address recent integration issue - show we care
       2. Review usage metrics - they're using 85% capacity
       3. Present Pro Plan benefits - they're hitting limits
       4. Discuss renewal terms (coming up soon)
       
       **Key Contact**
       • John Smith, IT Director (decision maker)
       • Mary Johnson, Operations (champion)
       
       Would you like me to draft an agenda or 
       prepare specific materials?
```

**Conversation 2: Proposal Draft**
```
Sales Rep: Create a proposal for Acme Corp for the Pro Plan upgrade

Agent: 📝 **Drafting Proposal for Acme Corp**
       
       Let me gather the details...
       
       ✅ Customer: Acme Corp
       ✅ Current Plan: Basic ($2,400/year)
       ✅ Proposed: Pro Plan ($8,500/year)
       ✅ Upgrade Value: Additional features + higher limits
       
       I'll create a draft based on our Pro Plan template.
       
       ---
       
       **DRAFT PROPOSAL**
       
       **Prepared for:** Acme Corp
       **Prepared by:** Sarah Johnson
       **Date:** February 2, 2026
       
       **Executive Summary**
       Based on your current usage and growth trajectory, 
       we recommend upgrading to our Pro Plan...
       
       [Draft continues with standard sections]
       
       **Investment**
       • Pro Plan Annual: $8,500
       • Less: Loyalty Discount (10%): -$850
       • Your Investment: $7,650/year
       
       ---
       
       ⚠️ **This is a draft - please review before sending**
       
       • Edit this proposal: [Open in Word]
       • Request manager approval for discount
       • Generate PDF version
       
       Shall I update the opportunity in CRM to 
       "Proposal Sent" after you finalize?
```

---

## Trust Configuration

```json
{
  "trust_config": {
    "level": 2,
    "name": "Sales Assistant",
    
    "autonomous_actions": [
      "search_products",
      "retrieve_customer_data",
      "generate_drafts",
      "provide_information"
    ],
    
    "requires_approval": [
      "update_crm",
      "send_proposal",
      "apply_discount",
      "schedule_customer_meeting"
    ],
    
    "read_only_systems": [
      "crm_customer_data",
      "crm_opportunities",
      "crm_activities"
    ],
    
    "draft_only": [
      "proposals",
      "emails",
      "quotes"
    ]
  }
}
```

---

## Success Metrics

| Metric | Target |
|--------|--------|
| Time Saved per Rep | 5 hours/week |
| Proposal Creation Time | 50% reduction |
| CRM Data Quality | 20% improvement |
| Sales Rep Satisfaction | 4.5/5 |
| Information Accuracy | 98% |

---

## Post-Workshop Roadmap

1. **Week 1-2:** Deploy product info assistant
2. **Week 3-4:** Add proposal drafting
3. **Month 2:** CRM read integration
4. **Month 3:** CRM write with approval workflow

---

*This scenario is ideal for sales organizations looking to increase rep productivity and reduce administrative burden.*
