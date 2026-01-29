# 🔧 Environment Setup Guide

This guide helps you set up the technical environment needed for an Agentathon.

---

## 📋 Prerequisites

### Required Licenses

| Component | Requirement |
|-----------|-------------|
| Microsoft 365 | Business Premium or Enterprise |
| Copilot Studio | Copilot Studio license per participant |
| Azure | Azure subscription (for advanced scenarios) |
| Power Platform | Environment with Dataverse |

### Recommended Setup

Each participant should have:
- [ ] Valid Microsoft 365 account
- [ ] Copilot Studio access
- [ ] Power Platform environment access
- [ ] Web browser (Edge or Chrome recommended)

---

## 🛠️ Step-by-Step Setup

### 1. Verify Copilot Studio Access

1. Navigate to [copilotstudio.microsoft.com](https://copilotstudio.microsoft.com)
2. Sign in with your organizational account
3. Verify you can see the home page
4. Check you can create a new agent

### 2. Create Environment

For workshops, we recommend creating a dedicated environment:

1. Go to [Power Platform Admin Center](https://admin.powerplatform.microsoft.com)
2. Select **Environments** > **+ New**
3. Configure:
   - **Name**: Agentathon-[Date]
   - **Type**: Sandbox
   - **Purpose**: Training
   - **Create Database**: Yes

### 3. Configure Connectors

Depending on your use cases, you may need:

| Connector | Purpose |
|-----------|---------|
| SharePoint | Document access |
| Dataverse | Data storage |
| HTTP | External API calls |
| Azure OpenAI | Custom AI capabilities |

### 4. Prepare Sample Data

For hands-on exercises:

1. Create sample SharePoint site with documents
2. Prepare FAQ content for knowledge bases
3. Set up sample database tables in Dataverse

---

## 🧪 Testing Checklist

Before the event, verify each participant can:

- [ ] Access Copilot Studio
- [ ] Create a new agent
- [ ] Add knowledge sources
- [ ] Test the agent
- [ ] Publish to a channel (Teams, Web)

---

## ⚠️ Common Issues & Solutions

### Issue: User cannot access Copilot Studio

**Solution**: Verify the user has a Copilot Studio license assigned in Microsoft 365 Admin Center.

### Issue: Cannot create new environment

**Solution**: Check Power Platform capacity. Contact your tenant admin.

### Issue: Connectors not available

**Solution**: Verify data loss prevention (DLP) policies in the tenant allow required connectors.

---

## 📞 Support Contacts

- **Microsoft Support**: [support.microsoft.com](https://support.microsoft.com)
- **Power Platform Admin Center**: [admin.powerplatform.microsoft.com](https://admin.powerplatform.microsoft.com)
- **Internal IT Team**: [Placeholder - Your IT Contact]

---

## 📝 Environment Details

Document your environment details here:

| Item | Value |
|------|-------|
| Environment Name | [Your environment] |
| Environment URL | [URL] |
| Admin Contact | [Contact] |
| Backup Environment | [If applicable] |
