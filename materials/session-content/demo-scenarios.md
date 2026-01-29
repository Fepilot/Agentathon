# 🎬 Demo Scenarios

Pre-built scenarios for demonstrations and reference during Agentathons.

---

## 📋 Scenario Overview

| # | Scenario | Industry | Complexity |
|---|----------|----------|------------|
| 1 | HR Policy Assistant | All | Simple |
| 2 | IT Support Agent | All | Medium |
| 3 | Customer Order Tracker | Retail | Medium |
| 4 | Employee Onboarding | All | Complex |

---

## Scenario 1: HR Policy Assistant

### Overview

An agent that answers employee questions about HR policies, benefits, and procedures.

### Use Case

**User Story**: As an employee, I want to quickly get answers about company policies without searching through documents or waiting for HR to respond.

### Sample Interactions

```
User: "How many vacation days do I get?"
Agent: "Based on our company policy, full-time employees receive 
       20 vacation days per year. Part-time employees receive 
       vacation days prorated based on their hours..."

User: "What's the process for requesting time off?"
Agent: "To request time off, follow these steps:
       1. Log into the HR portal
       2. Navigate to 'Time Off Requests'
       3. Select your dates and type of leave
       4. Submit for manager approval
       Would you like me to provide the link to the portal?"
```

### Knowledge Sources
- HR Policy document
- Employee handbook
- Benefits guide

### Actions (Optional)
- Link to HR portal
- Send notification to HR team

### Build Guide

1. **Create Agent**
   - Name: "HR Assistant"
   - Instructions: "You are a helpful HR assistant for [Company]. Answer questions about policies, benefits, and HR procedures."

2. **Add Knowledge**
   - Upload HR policy documents
   - Connect to HR SharePoint site

3. **Test Questions**
   - Vacation policy
   - Sick leave process
   - Benefits enrollment
   - Expense reimbursement

---

## Scenario 2: IT Support Agent

### Overview

An agent that helps employees troubleshoot common IT issues and submit support tickets.

### Use Case

**User Story**: As an employee, I want to quickly resolve common IT issues and easily submit tickets for complex problems.

### Sample Interactions

```
User: "My computer is running slowly"
Agent: "I can help with that! Let's try some troubleshooting steps:
       1. Close any unused applications
       2. Restart your computer
       3. Check available disk space
       
       Did any of these help?"

User: "No, it's still slow"
Agent: "I'll create a support ticket for you. 
       Please provide:
       - Your computer model
       - When did this start?
       - Any recent software installations?"

User: "Dell Latitude, started Monday, no new software"
Agent: "I've created ticket #IT-2024-1234 for you.
       A technician will contact you within 4 hours.
       Is there anything else I can help with?"
```

### Knowledge Sources
- IT troubleshooting guides
- FAQ documents
- Known issues database

### Actions
- Create support ticket (Dataverse/ServiceNow)
- Send confirmation email
- Check ticket status

### Build Guide

1. **Create Agent**
   - Name: "IT Support Bot"
   - Instructions: "You are an IT support assistant. Help users troubleshoot common issues and create tickets when needed."

2. **Create Topics**
   - Password reset
   - Slow computer
   - Network issues
   - Software requests

3. **Add Actions**
   - Create ticket flow
   - Status lookup flow

---

## Scenario 3: Customer Order Tracker

### Overview

An agent that helps customers track their orders and handle common inquiries.

### Use Case

**User Story**: As a customer, I want to easily check my order status and get quick answers to shipping questions.

### Sample Interactions

```
User: "Where is my order?"
Agent: "I'd be happy to help you track your order!
       Please provide your order number or the email 
       used for the order."

User: "Order #123456"
Agent: "I found your order! Here's the status:
       📦 Order #123456
       ✅ Status: Shipped
       🚚 Carrier: FedEx
       📍 Last Location: Distribution Center, Madrid
       📅 Expected Delivery: January 30, 2026
       
       Would you like the tracking link?"
```

### Knowledge Sources
- Shipping FAQ
- Return policy
- Product catalog

### Actions
- Look up order (API call)
- Initiate return
- Connect to support

### Build Guide

1. **Create Agent**
   - Name: "Order Assistant"
   - Instructions: "You help customers track orders and answer shipping questions. Always be friendly and helpful."

2. **Add Knowledge**
   - Shipping policy
   - FAQ documents

3. **Create Actions**
   - Order lookup (HTTP connector)
   - Return initiation flow

---

## Scenario 4: Employee Onboarding Assistant

### Overview

A comprehensive agent that guides new employees through their first weeks, answering questions and pointing them to resources.

### Use Case

**User Story**: As a new employee, I want a friendly guide to help me navigate my first weeks and find the information I need.

### Sample Interactions

```
User: "I'm starting next week. What should I know?"
Agent: "Welcome to [Company]! 🎉 I'm your onboarding assistant.
       
       Here's what to expect in your first week:
       
       📅 Day 1:
       - Arrive at 9 AM at reception
       - IT setup and badge collection
       - Meet your manager
       - Team lunch
       
       📅 Week 1 Tasks:
       - Complete compliance training
       - Set up benefits enrollment
       - Attend new hire orientation
       
       What would you like to know more about?"

User: "How do I set up my email?"
Agent: "To set up your email:
       1. Open Outlook on your laptop
       2. Enter your company email: [name]@company.com
       3. Use the temporary password from IT
       4. Follow prompts to set your new password
       
       If you have issues, the IT Help Desk is at extension 1234."
```

### Knowledge Sources
- Onboarding guide
- IT setup instructions
- Benefits information
- Company culture documents
- Office maps and locations

### Actions
- Training enrollment
- Meeting scheduling
- Equipment requests

### Build Guide

1. **Create Agent**
   - Name: "Onboarding Buddy"
   - Instructions: "You are a friendly onboarding assistant. Help new employees feel welcome and find information easily."

2. **Add Extensive Knowledge**
   - Multiple onboarding documents
   - IT setup guides
   - HR policies

3. **Create Topics**
   - First day checklist
   - IT setup help
   - Benefits questions
   - Training enrollment

---

## 📝 Demo Tips

### Before the Demo

- [ ] Test all scenarios
- [ ] Clear chat history
- [ ] Prepare backup questions
- [ ] Have fallback plan

### During the Demo

- Start with a simple question
- Show knowledge retrieval
- Demonstrate an action
- Show error handling

### After the Demo

- Invite questions
- Explain customization options
- Share next steps

---

## 🔧 Troubleshooting Common Issues

| Issue | Solution |
|-------|----------|
| Agent doesn't understand | Improve trigger phrases |
| Wrong information returned | Check knowledge source quality |
| Action fails | Verify connector configuration |
| Slow response | Optimize knowledge sources |
