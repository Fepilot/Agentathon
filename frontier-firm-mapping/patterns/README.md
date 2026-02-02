# 🎯 Agent Pattern Templates

> Ready-to-use templates for building agents aligned with Frontier Firm patterns

---

## Overview

This folder contains configuration templates and starting points for building agents based on the 10 key automation patterns from the Frontier Firm Playbook.

---

## Available Templates

| Pattern | Template | Status |
|---------|----------|--------|
| Pattern 4: Customer Support | [customer-service-template.json](./customer-service-template.json) | ✅ Ready |
| Pattern 5: HR Operations | [hr-operations-template.json](./hr-operations-template.json) | ✅ Ready |
| Pattern 7: IT Service Desk | [it-service-template.json](./it-service-template.json) | ✅ Ready |
| Pattern 8: Sales Enablement | [sales-enablement-template.json](./sales-enablement-template.json) | ✅ Ready |
| Pattern 6: Back-Office | [back-office-template.json](./back-office-template.json) | ✅ Ready |

---

## Template Structure

Each template includes:

```json
{
  "pattern_info": {
    "name": "Pattern Name",
    "pattern_number": 4,
    "description": "What this pattern addresses",
    "typical_horizon": "H2",
    "recommended_trust_level": "L2"
  },
  
  "agent_config": {
    "name": "Agent Name",
    "description": "Agent description",
    "icon": "🎯",
    "primary_language": "en-US"
  },
  
  "topics": [
    {
      "name": "Topic Name",
      "trigger_phrases": ["phrase 1", "phrase 2"],
      "flow_description": "What this topic does"
    }
  ],
  
  "knowledge_sources": [
    {
      "type": "sharepoint",
      "description": "What content to include"
    }
  ],
  
  "trust_config": {
    "initial_level": 2,
    "autonomous_actions": [],
    "requires_approval": [],
    "escalation_triggers": []
  },
  
  "success_metrics": {
    "primary": [],
    "secondary": []
  },
  
  "implementation_notes": "Tips for building this agent"
}
```

---

## How to Use Templates

### Step 1: Choose Your Pattern
Select the template that matches your use case

### Step 2: Customize Configuration
- Update agent name and description
- Modify trigger phrases for your domain
- Adjust trust levels based on your risk tolerance

### Step 3: Prepare Knowledge Base
- Gather documents listed in `knowledge_sources`
- Format for Copilot Studio ingestion

### Step 4: Build in Copilot Studio
- Create new agent
- Add topics from template
- Configure connectors and actions

### Step 5: Test and Refine
- Test with sample conversations
- Adjust based on results
- Iterate trust levels

---

## Creating Custom Templates

Use this base structure:

```json
{
  "pattern_info": {
    "name": "",
    "description": "",
    "typical_horizon": "",
    "recommended_trust_level": ""
  },
  "agent_config": {},
  "topics": [],
  "knowledge_sources": [],
  "trust_config": {},
  "success_metrics": {},
  "implementation_notes": ""
}
```

---

*Templates are starting points - customize for your specific organizational needs.*
