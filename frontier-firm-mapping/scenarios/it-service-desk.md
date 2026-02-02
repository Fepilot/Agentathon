# 🔧 IT Service Desk Automation Scenario

> Provide instant IT support and reduce ticket volume with intelligent automation

---

## Overview

This scenario focuses on building an IT support agent that handles common technical issues, guides users through troubleshooting, and intelligently routes complex issues.

**Pattern:** IT Service Management (Pattern 7)  
**Horizon:** H2 (Workflow Automation)  
**Trust Level:** L2 → L3  
**Duration:** 2 days  
**Complexity:** Medium

---

## Business Context

### The Challenge
- IT teams overwhelmed with repetitive tickets
- Password resets consume significant time
- Users wait hours for simple fixes
- Knowledge scattered across multiple systems
- After-hours support is limited and expensive

### The Solution
An IT support agent that:
- Auto-resolves 40%+ of common issues
- Guides users through self-service troubleshooting
- Creates and routes tickets appropriately
- Provides 24/7 first-line support
- Learns from resolution patterns

---

## Objectives

By the end of this Agentathon, participants will have built:

- [ ] IT support agent in Copilot Studio
- [ ] Self-service troubleshooting guides
- [ ] Automated password reset workflow
- [ ] Ticket creation and routing
- [ ] Integration with IT service management tool

---

## Technical Implementation

### Agent Structure

```
IT Support Agent
├── System Topics
│   ├── Greeting
│   ├── Goodbye
│   ├── Escalate (→ IT Team)
│   └── Fallback
│
├── Self-Service Topics
│   ├── Password Reset
│   ├── VPN Troubleshooting
│   ├── Email/Outlook Issues
│   ├── Printer Setup
│   ├── Software Installation
│   ├── Teams/Meeting Issues
│   └── Network Connectivity
│
├── Request Topics
│   ├── New Equipment Request
│   ├── Software Request
│   ├── Access Request
│   └── Report an Outage
│
├── Knowledge Sources
│   ├── IT Knowledge Base
│   ├── Troubleshooting Guides
│   └── FAQ Document
│
└── Actions
    ├── Verify User Identity
    ├── Initiate Password Reset
    ├── Create Ticket (ServiceNow/Jira)
    ├── Check System Status
    └── Send Confirmation Email
```

### Key Topics

#### Topic 1: Password Reset
```yaml
name: Password Reset
trigger_phrases:
  - "Reset my password"
  - "Forgot password"
  - "Can't log in"
  - "Password expired"
  - "Account locked"

trust_level: L3 (can execute automatically with verification)

conversation_flow:
  1. Verify user identity (email + employee ID)
  2. Confirm which system (AD, VPN, application)
  3. Initiate password reset
  4. Provide temporary password or reset link
  5. Confirm completion

security_measures:
  - Verify employee ID matches email
  - Send confirmation to registered email
  - Log all reset attempts
  - Limit to 3 attempts per hour
```

#### Topic 2: VPN Troubleshooting
```yaml
name: VPN Troubleshooting
trigger_phrases:
  - "VPN not working"
  - "Can't connect to VPN"
  - "VPN slow"
  - "Remote access issues"

conversation_flow:
  1. Ask about specific error/symptoms
  2. Check known outages
  3. Guide through troubleshooting steps
  4. Verify resolution
  5. Create ticket if unresolved

troubleshooting_steps:
  - Restart VPN client
  - Check internet connection
  - Verify credentials
  - Clear VPN cache
  - Reinstall VPN client
```

### Sample Conversations

**Conversation 1: Password Reset (Automated)**
```
User: I need to reset my password

Agent: I can help you reset your password. 
       For security, I'll need to verify your identity.
       
       What's your employee ID?

User: EMP12345

Agent: Thanks! And which system do you need the password reset for?
       
       • Windows/Network login
       • VPN
       • Email
       • Other application

User: Windows login

Agent: 🔐 Verifying your identity...
       
       ✅ Verified: John Smith (EMP12345)
       
       I'm initiating your Windows password reset now.
       
       ✅ Password reset initiated!
       
       📧 I've sent a password reset link to your registered 
       email (j.smith@company.com).
       
       The link will expire in 15 minutes.
       
       **Next steps:**
       1. Check your email
       2. Click the reset link
       3. Create a new password (min 12 characters, including 
          uppercase, number, and symbol)
       
       ⚠️ If you don't receive the email within 5 minutes, 
       check your spam folder or let me know.
       
       Is there anything else I can help with?
```

**Conversation 2: Guided Troubleshooting**
```
User: My VPN isn't working

Agent: I'm sorry to hear you're having VPN issues. 
       Let me help you troubleshoot.
       
       First, what's happening when you try to connect?
       
       • Connection times out
       • Wrong password error
       • Connects but no network access
       • Client won't launch
       • Other

User: Connection times out

Agent: Let's try a few things. First, let me check if 
       there are any known VPN outages...
       
       ✅ VPN Status: All systems operational
       
       Let's troubleshoot step by step:
       
       **Step 1: Restart VPN Client**
       1. Right-click the VPN icon in your system tray
       2. Select "Quit" or "Exit"
       3. Wait 10 seconds
       4. Relaunch the VPN client
       5. Try connecting again
       
       Did this resolve the issue?

User: No, still timing out

Agent: Let's try the next step:
       
       **Step 2: Clear VPN Cache**
       1. Close the VPN client completely
       2. Press Windows + R
       3. Type: %appdata%\VPNClient
       4. Delete the "cache" folder
       5. Restart your computer
       6. Try connecting again
       
       Did this help?

User: No

Agent: Since the basic troubleshooting didn't resolve this,
       let me create a ticket for our network team.
       
       🎫 **Creating IT Ticket**
       
       Issue: VPN connection timeout
       Priority: Medium
       Steps tried: Client restart, cache clear
       
       Ticket created: INC0012345
       
       A network specialist will contact you within 2 hours.
       You can track your ticket at [IT Portal](link).
       
       In the meantime, can you work from the office or 
       use the web portal as an alternative?
```

---

## Trust Configuration

```json
{
  "trust_config": {
    "level": 2,
    
    "autonomous_actions_L3": [
      "password_reset_with_verification",
      "provide_troubleshooting_guides",
      "check_system_status",
      "send_confirmation_emails"
    ],
    
    "requires_ticket_L2": [
      "hardware_issues",
      "software_installation",
      "access_requests",
      "network_issues"
    ],
    
    "immediate_escalation": [
      "security_incident",
      "data_breach_suspected",
      "executive_request",
      "system_wide_outage"
    ],
    
    "security_controls": {
      "identity_verification": "required",
      "audit_logging": "all_actions",
      "sensitive_actions_mfa": true,
      "rate_limiting": true
    }
  }
}
```

---

## Success Metrics

| Metric | Target |
|--------|--------|
| Auto-Resolution Rate | 40% |
| First Contact Resolution | 70% |
| Average Resolution Time | <5 min for auto-resolved |
| Ticket Volume Reduction | 30% |
| User Satisfaction | 4.5/5 |

---

## Post-Workshop Roadmap

1. **Week 1-2:** Deploy password reset only (highest volume, lowest risk)
2. **Week 3-4:** Add troubleshooting guides
3. **Month 2:** Integrate with ITSM for ticket creation
4. **Month 3:** Add proactive monitoring alerts

---

*This scenario is ideal for IT organizations looking to reduce ticket volume and improve response times.*
