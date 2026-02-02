# 🎫 Customer Service Excellence Scenario

> Transform customer support with AI agents that handle inquiries, provide instant responses, and continuously learn

---

## Overview

This scenario focuses on building a comprehensive customer service agent that can handle common inquiries, provide accurate information, and seamlessly escalate complex issues to human agents.

**Pattern:** Customer Support (Pattern 4)  
**Horizon:** H2 (Workflow Automation)  
**Trust Level:** L2 → L3  
**Duration:** 2 days  
**Complexity:** Medium

---

## Business Context

### The Challenge
- High volume of repetitive customer inquiries
- Long wait times during peak periods
- Inconsistent responses across agents
- Limited to business hours
- Rising customer expectations for instant service

### The Solution
An AI agent that:
- Handles 50%+ of inquiries automatically
- Provides instant, consistent responses
- Available 24/7
- Escalates appropriately when needed
- Learns from interactions to improve

---

## Objectives

By the end of this Agentathon, participants will have built:

- [ ] A working customer service agent in Copilot Studio
- [ ] Knowledge base integration with company FAQs
- [ ] Escalation workflow to human agents
- [ ] Multi-channel deployment (web chat, Teams)
- [ ] Basic analytics and reporting

---

## Prerequisites

### Technical Requirements
- Copilot Studio environment (CDX or customer tenant)
- Microsoft 365 licenses for participants
- Access to sample customer service data/FAQs

### Knowledge Base Preparation
Prepare these before the Agentathon:
- [ ] Top 50 customer FAQs with answers
- [ ] Product/service catalog information
- [ ] Return/refund policies
- [ ] Contact information and hours
- [ ] Escalation criteria and routing rules

### Participant Preparation
- Complete Copilot Studio fundamentals (2 hours)
- Review customer service metrics and pain points
- Identify 3-5 priority use cases to automate

---

## Agenda

### Day 1: Discovery & Design

| Time | Activity | Description |
|------|----------|-------------|
| 09:00 | Welcome & Introductions | Agenda, objectives, team formation |
| 09:30 | AI Agents Overview | What agents can do, Frontier Firm context |
| 10:00 | Copilot Studio Demo | Live demonstration of capabilities |
| 10:30 | ☕ Break | |
| 10:45 | Use Case Discovery | Map customer service journey, identify automation opportunities |
| 12:00 | Horizon & Trust Assessment | Classify use cases, define trust levels |
| 12:30 | 🍽️ Lunch | |
| 13:30 | Agent Design Workshop | Design conversation flows, define topics |
| 15:00 | Knowledge Base Setup | Import FAQs, organize content |
| 15:30 | ☕ Break | |
| 15:45 | Hands-on Building Begins | Create agent, first topics |
| 17:00 | Day 1 Wrap-up | Progress review, questions |

### Day 2: Build & Demo

| Time | Activity | Description |
|------|----------|-------------|
| 09:00 | Day 1 Recap | Review progress, address blockers |
| 09:15 | Continue Building | Complete primary topics |
| 10:30 | ☕ Break | |
| 10:45 | Escalation Workflow | Build human handoff flow |
| 12:00 | Integration Setup | Connect to systems (if applicable) |
| 12:30 | 🍽️ Lunch | |
| 13:30 | Testing & Refinement | Test scenarios, fix issues |
| 15:00 | Analytics Setup | Configure tracking and metrics |
| 15:30 | ☕ Break | |
| 15:45 | Demo Preparation | Prepare presentation |
| 16:00 | Demo Presentations | Teams present their agents |
| 16:45 | Next Steps & Roadmap | Production path, graduation criteria |
| 17:00 | Closing | Certificates, feedback |

---

## Technical Implementation

### Agent Structure

```
Customer Service Agent
├── System Topics (built-in)
│   ├── Greeting
│   ├── Goodbye
│   ├── Escalate
│   └── Fallback
│
├── Custom Topics
│   ├── Order Status
│   ├── Return Request
│   ├── Product Information
│   ├── Store Hours/Locations
│   ├── Shipping Information
│   ├── Payment Issues
│   └── General FAQ
│
├── Knowledge Base
│   ├── FAQ Document
│   ├── Product Catalog
│   └── Policy Documents
│
└── Actions
    ├── Look Up Order (API/connector)
    ├── Create Ticket (Dynamics/ServiceNow)
    └── Send Email Confirmation
```

### Topics to Create

#### Topic 1: Order Status
```yaml
name: Order Status
trigger_phrases:
  - "Where is my order"
  - "Track my package"
  - "Order status"
  - "When will my order arrive"
  - "Shipping update"

conversation_flow:
  1. Ask for order number (if not provided)
  2. Validate order number format
  3. Call order lookup action
  4. Present order status with details
  5. Offer additional help

variables:
  - order_number (string)
  - order_status (string)
  - estimated_delivery (date)

escalation_trigger:
  - Order not found after 3 attempts
  - Delivery significantly delayed
  - Customer expresses frustration
```

#### Topic 2: Return Request
```yaml
name: Return Request
trigger_phrases:
  - "I want to return"
  - "Return policy"
  - "How do I return"
  - "Exchange item"
  - "Refund request"

conversation_flow:
  1. Ask for order number
  2. Verify purchase date (within return window)
  3. Ask reason for return
  4. Explain return process
  5. Generate return label (if applicable)
  6. Confirm next steps

trust_level: L2 (requires approval for refunds over threshold)

escalation_trigger:
  - Outside return window (manager approval needed)
  - High-value item
  - Damaged product claim
```

#### Topic 3: Product Information
```yaml
name: Product Information
trigger_phrases:
  - "Tell me about [product]"
  - "Product specifications"
  - "Is [product] available"
  - "Compare products"
  - "Product recommendations"

conversation_flow:
  1. Identify product of interest
  2. Search knowledge base
  3. Present product information
  4. Offer to check availability
  5. Provide purchase options

knowledge_source: Product catalog document
```

### Sample Conversations

**Conversation 1: Order Status (Happy Path)**
```
Customer: Hi, where is my order?

Agent: Hello! I'd be happy to help you track your order. 
       Could you please provide your order number? 
       It usually starts with "ORD-" followed by 8 digits.

Customer: ORD-12345678

Agent: Thank you! Let me look that up for you...
       
       ✅ Order Found: ORD-12345678
       
       📦 Status: In Transit
       🚚 Carrier: FedEx
       📅 Estimated Delivery: February 4, 2026
       
       Your package is currently at the local distribution center 
       and is on schedule for delivery.
       
       Is there anything else I can help you with?

Customer: No, that's all. Thanks!

Agent: You're welcome! Have a great day! 
       If you have any other questions, I'm here to help.
```

**Conversation 2: Return Request (Escalation)**
```
Customer: I need to return something

Agent: I'd be happy to help with your return. 
       Could you please provide your order number?

Customer: ORD-87654321

Agent: Thank you! I found your order from January 5, 2026.
       
       What item would you like to return?

Customer: The laptop - it's defective

Agent: I'm sorry to hear that your laptop isn't working properly. 
       Since this involves a defective electronics item, I want to make 
       sure you get the best support possible.
       
       🔄 I'm connecting you with a specialist who can help with 
       warranty claims and ensure you get a proper replacement.
       
       Please hold for just a moment...
       
       [Escalated to: Tech Support Queue]
       [Reason: Defective high-value item]
       [Context: Order ORD-87654321, laptop, defective claim]
```

---

## Trust Configuration

### Initial Trust Level: L2 (Supervised)

```json
{
  "trust_config": {
    "level": 2,
    "name": "Supervised",
    
    "autonomous_actions": [
      "provide_information",
      "look_up_order",
      "share_policy",
      "answer_faq"
    ],
    
    "requires_approval": [
      "process_refund",
      "create_exception",
      "modify_order"
    ],
    
    "always_escalate": [
      "legal_mention",
      "threat_detected",
      "vip_customer",
      "media_mention"
    ],
    
    "escalation_triggers": {
      "keywords": ["lawyer", "sue", "complaint", "manager", "supervisor"],
      "sentiment_threshold": -0.6,
      "confidence_below": 0.7,
      "repeat_attempts": 3
    }
  }
}
```

### Graduation Path to L3

| Metric | Threshold | Timeline |
|--------|-----------|----------|
| Interactions | 1,000+ | 4 weeks |
| Accuracy | >95% | Sustained |
| Customer Satisfaction | >4.5/5 | Average |
| Escalation Accuracy | >90% | Appropriate escalations |
| Zero Critical Errors | 0 | Entire period |

---

## Success Metrics

### Primary KPIs

| Metric | Baseline | Target | Measurement |
|--------|----------|--------|-------------|
| Deflection Rate | 0% | 50% | % handled without human |
| First Response Time | 15 min | <30 sec | Average time to first response |
| Resolution Time | 45 min | 5 min | Average time to resolution |
| Customer Satisfaction | 4.0 | 4.5+ | Post-interaction survey |
| Cost per Interaction | €8 | €2 | Total cost / interactions |

### Secondary KPIs

| Metric | Target |
|--------|--------|
| Knowledge Base Coverage | 90% of queries answered |
| Escalation Rate | <30% |
| Accurate Escalations | >90% |
| Agent Availability | 99.9% uptime |
| User Adoption | 80% of customers use chat |

---

## Common Challenges

### Challenge 1: Knowledge Base Gaps
**Symptom:** Agent frequently says "I don't know"
**Solution:** 
- Track unknown queries
- Weekly knowledge base updates
- Implement feedback loop

### Challenge 2: Over-Escalation
**Symptom:** Agent escalates too many queries
**Solution:**
- Review escalation triggers
- Add more topics/training
- Adjust confidence thresholds

### Challenge 3: Under-Escalation
**Symptom:** Customers frustrated, needed human help
**Solution:**
- Add sentiment analysis
- Include explicit escalation option
- Review missed escalations

### Challenge 4: Context Loss
**Symptom:** Agent doesn't remember earlier conversation
**Solution:**
- Implement proper variable handling
- Use conversation summary
- Ensure context passed on escalation

---

## Post-Workshop Roadmap

### Week 1-2: Refinement
- [ ] Analyze workshop feedback
- [ ] Fix identified issues
- [ ] Add missing topics
- [ ] Expand knowledge base

### Week 3-4: Pilot
- [ ] Deploy to limited user group (10%)
- [ ] Collect feedback daily
- [ ] Monitor all metrics
- [ ] Quick iterations

### Month 2: Expanded Pilot
- [ ] Increase to 50% of traffic
- [ ] Add additional channels
- [ ] Integrate with CRM
- [ ] Prepare for full rollout

### Month 3: Production
- [ ] Full deployment
- [ ] Graduate to L3 (if metrics achieved)
- [ ] Establish ongoing improvement process
- [ ] Plan next Agentathon use cases

---

## Resources

- [Customer Service Agent Template](../patterns/customer-service-template.md)
- [Knowledge Base Best Practices](../../materials/prerequisites/knowledge-base-guide.md)
- [Escalation Design Guide](../../materials/session-content/escalation-design.md)

---

*This scenario is designed for organizations looking to transform their customer service operations with AI agents.*
