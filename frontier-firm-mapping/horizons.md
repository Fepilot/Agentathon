# 📊 The Three Horizons Framework - Deep Dive

> Understanding where your AI agents fit in the enterprise transformation journey

---

## Overview

The Three Horizons Framework helps organizations classify AI agent initiatives based on their autonomy level, complexity, and business impact. This classification is crucial for:

- Setting appropriate expectations
- Defining trust boundaries
- Planning resource allocation
- Measuring success appropriately

---

## Horizon 1: Individual Productivity

### Definition
AI assistants that augment individual workers, providing suggestions and automating simple tasks while keeping humans fully in control.

### Characteristics

| Aspect | Description |
|--------|-------------|
| **Autonomy** | Low - Human approves all actions |
| **Complexity** | Single-step or simple multi-step tasks |
| **Risk** | Low - Easy to review and correct |
| **Integration** | Standalone or light integration |
| **Training Need** | Minimal - Intuitive interfaces |

### Examples for Agentathon

```
┌─────────────────────────────────────────────────────────────────┐
│                    HORIZON 1 AGENTS                             │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  📝 Document Assistant                                          │
│     • Drafts emails based on bullet points                      │
│     • Summarizes long documents                                 │
│     • Suggests improvements to writing                          │
│     Human: Reviews and sends                                    │
│                                                                 │
│  🔍 Search & Retrieve Agent                                     │
│     • Finds relevant policies/documents                         │
│     • Answers factual questions from knowledge base             │
│     • Provides links to sources                                 │
│     Human: Validates and uses information                       │
│                                                                 │
│  📊 Data Lookup Agent                                           │
│     • Retrieves information from databases                      │
│     • Formats data for reports                                  │
│     • Creates basic visualizations                              │
│     Human: Interprets and acts on data                          │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Agentathon Implementation Tips

1. **Quick Wins**: Start here for participants new to agent building
2. **Focus**: User interface and response quality
3. **Success Metric**: User adoption and satisfaction
4. **Trust Level**: L1 (Shadowing) to L2 (Supervised)

### Sample Copilot Studio Configuration

```yaml
# Horizon 1 Agent Settings
agent:
  name: "Document Assistant"
  horizon: 1
  
topics:
  - name: "Draft Email"
    trigger: "Help me write an email about..."
    actions:
      - generate_draft
      - present_to_user  # Human reviews before any action
      
  - name: "Summarize Document"
    trigger: "Summarize this document..."
    actions:
      - extract_key_points
      - generate_summary
      - present_to_user  # Human uses as they see fit

settings:
  requires_human_approval: true
  can_take_external_actions: false
  max_response_length: 500
```

---

## Horizon 2: Workflow Automation

### Definition
AI agents that automate multi-step workflows, orchestrating tasks across systems while maintaining human oversight at key decision points.

### Characteristics

| Aspect | Description |
|--------|-------------|
| **Autonomy** | Medium - Executes within defined boundaries |
| **Complexity** | Multi-step workflows, multiple systems |
| **Risk** | Medium - Requires checkpoints and rollback |
| **Integration** | Connected to enterprise systems |
| **Training Need** | Moderate - Process understanding needed |

### Examples for Agentathon

```
┌─────────────────────────────────────────────────────────────────┐
│                    HORIZON 2 AGENTS                             │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  🎫 Customer Service Pipeline                                   │
│     Step 1: Receive and parse customer inquiry                  │
│     Step 2: Search knowledge base for solution                  │
│     Step 3: Draft personalized response                         │
│     Step 4: [CHECKPOINT] Human reviews response                 │
│     Step 5: Send response and log interaction                   │
│     Step 6: Update knowledge base if new pattern                │
│                                                                 │
│  📋 Invoice Processing Agent                                    │
│     Step 1: Extract data from invoice (OCR/AI)                  │
│     Step 2: Validate against purchase orders                    │
│     Step 3: Route based on amount/category                      │
│     Step 4: [CHECKPOINT] Approval for exceptions                │
│     Step 5: Process payment                                     │
│     Step 6: Update accounting system                            │
│                                                                 │
│  👥 Employee Onboarding Agent                                   │
│     Step 1: Receive new hire notification                       │
│     Step 2: Create accounts across systems                      │
│     Step 3: Send welcome materials                              │
│     Step 4: Schedule orientation sessions                       │
│     Step 5: [CHECKPOINT] Manager confirms completion            │
│     Step 6: Follow up on first-week experience                  │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Agentathon Implementation Tips

1. **Design First**: Map the complete workflow before building
2. **Identify Checkpoints**: Where must humans approve?
3. **Error Handling**: What happens when something fails?
4. **Integration Planning**: Which connectors are needed?
5. **Trust Level**: L2 (Supervised) to L3 (Autonomous for low-risk steps)

### Sample Workflow Architecture

```
┌──────────────────────────────────────────────────────────────────────────┐
│                    H2 WORKFLOW PATTERN                                   │
├──────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│   ┌─────────┐    ┌─────────┐    ┌─────────┐    ┌─────────┐             │
│   │ Trigger │───►│ Process │───►│ Decide  │───►│ Execute │             │
│   │         │    │         │    │         │    │         │             │
│   └─────────┘    └─────────┘    └────┬────┘    └─────────┘             │
│                                      │                                   │
│                                      ▼                                   │
│                               ┌─────────────┐                           │
│                               │  CHECKPOINT │                           │
│                               │   (Human)   │                           │
│                               └──────┬──────┘                           │
│                                      │                                   │
│                         ┌────────────┼────────────┐                     │
│                         ▼            ▼            ▼                     │
│                    ┌────────┐  ┌────────┐  ┌────────┐                  │
│                    │ Approve│  │ Modify │  │ Reject │                  │
│                    └────────┘  └────────┘  └────────┘                  │
│                                                                          │
└──────────────────────────────────────────────────────────────────────────┘
```

---

## Horizon 3: Autonomous Agents

### Definition
AI agents operating as "digital employees" with significant autonomy, making decisions and taking actions within defined boundaries, with human oversight through audit trails and exception handling.

### Characteristics

| Aspect | Description |
|--------|-------------|
| **Autonomy** | High - Acts independently within guardrails |
| **Complexity** | Complex decision-making, judgment calls |
| **Risk** | Higher - Requires robust safety measures |
| **Integration** | Deep system access, action authority |
| **Training Need** | Significant - Understanding boundaries |

### Examples for Agentathon (Future Vision)

```
┌─────────────────────────────────────────────────────────────────┐
│                    HORIZON 3 AGENTS                             │
├─────────────────────────────────────────────────────────────────┤
│                                                                 │
│  🤖 Autonomous Customer Success Agent                           │
│     • Monitors customer health scores continuously              │
│     • Proactively reaches out when issues detected              │
│     • Offers solutions, discounts, or escalates                 │
│     • Makes decisions up to defined authority level             │
│     • Human: Reviews weekly summaries, handles escalations      │
│                                                                 │
│  📈 Autonomous Trading/Pricing Agent                            │
│     • Monitors market conditions in real-time                   │
│     • Adjusts pricing within defined parameters                 │
│     • Executes transactions automatically                       │
│     • Human: Sets parameters, reviews performance               │
│                                                                 │
│  🔧 Autonomous IT Operations Agent                              │
│     • Monitors system health 24/7                               │
│     • Automatically remediates known issues                     │
│     • Scales resources based on demand                          │
│     • Human: Handles novel issues, reviews changes              │
│                                                                 │
└─────────────────────────────────────────────────────────────────┘
```

### Path to H3: Graduation Requirements

Before an agent reaches Horizon 3, it must demonstrate:

| Criterion | Threshold | Measurement |
|-----------|-----------|-------------|
| Accuracy | >98% | Sample review of decisions |
| Consistency | >99% | Same inputs → same outputs |
| Uptime | >99.9% | System monitoring |
| User Trust | >4.8/5 | User satisfaction surveys |
| Error Recovery | 100% | All errors handled gracefully |
| Audit Compliance | 100% | Full traceability |

### Agentathon Approach to H3

> ⚠️ **Note**: Most Agentathons should focus on H1-H2. H3 is typically achieved through gradual trust building post-workshop.

**During Agentathon:**
- Design with H3 potential in mind
- Implement comprehensive logging
- Define graduation criteria
- Create monitoring dashboards
- Document decision boundaries

**Post-Agentathon Path:**
```
H1 Prototype → H2 Pilot → H2 Production → H3 Candidate → H3 Production
   (Day 1-2)    (Week 2-4)   (Month 2-3)    (Month 4-6)    (Month 6+)
```

---

## Horizon Selection Guide

### Decision Matrix

```
                        LOW RISK                    HIGH RISK
                    ┌─────────────────────────┬─────────────────────────┐
                    │                         │                         │
    SIMPLE TASK     │     HORIZON 1           │     HORIZON 1           │
                    │     Quick win           │     Start safe          │
                    │     Fast deployment     │     Build trust first   │
                    │                         │                         │
                    ├─────────────────────────┼─────────────────────────┤
                    │                         │                         │
    COMPLEX         │     HORIZON 2-3         │     HORIZON 2           │
    WORKFLOW        │     Automation          │     Human checkpoints   │
                    │     opportunity         │     Careful graduation  │
                    │                         │                         │
                    └─────────────────────────┴─────────────────────────┘
```

### Quick Assessment Questions

1. **Can errors be easily reversed?**
   - Yes → Higher horizon possible
   - No → Start at H1

2. **Is there regulatory/compliance requirement?**
   - Yes → H1-H2 with audit trail
   - No → Faster progression possible

3. **Does the task require judgment?**
   - Rule-based → H2-H3 potential
   - Judgment-heavy → H1-H2

4. **What's the user expectation?**
   - Speed prioritized → Higher autonomy
   - Human touch expected → Lower autonomy

5. **Is there existing process documentation?**
   - Well-documented → Easier to automate
   - Tribal knowledge → More discovery needed

---

## Mapping Template

Use this template during Agentathon discovery sessions:

```markdown
## Use Case Horizon Assessment

**Use Case Name:** ________________________________

**Current Process:**
- Steps involved: ________________________________
- People involved: _______________________________
- Time per instance: _____________________________
- Volume (per day/week/month): ___________________

**Risk Assessment:**
- Impact of errors: [ ] Low [ ] Medium [ ] High
- Reversibility: [ ] Easy [ ] Moderate [ ] Difficult
- Regulatory requirements: [ ] None [ ] Some [ ] Strict

**Complexity Assessment:**
- Number of decision points: _____________________
- Integration needs: _____________________________
- Exception frequency: ___________________________

**Recommended Horizon:** [ ] H1 [ ] H2 [ ] H3

**Rationale:** __________________________________

**Trust Level to Start:** [ ] L1 [ ] L2 [ ] L3 [ ] L4

**Graduation Path:** ____________________________
```

---

*Next: [Trust Framework Implementation Guide](./trust-framework.md)*
