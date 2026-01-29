# 🔧 CDX Demo Tenant Setup for Agentathon

This guide explains how to set up a CDX (Customer Digital Experiences) demo tenant for running an Agentathon event.

---

## 📋 Overview

A **CDX Demo Tenant** provides a pre-configured Microsoft 365 environment with all the necessary licenses and data for running workshops. This is essential for Agentathons because:

- ✅ **Pre-configured licenses**: Copilot Studio, Power Platform, Microsoft 365
- ✅ **Sample data**: Ready-to-use content for building agents
- ✅ **Isolated environment**: No risk to production systems
- ✅ **Quick setup**: Get started in minutes, not days

---

## 📥 Download Full Guide

For detailed step-by-step instructions with screenshots, download the official guide:

**[📄 Download CDX Demo Tenant Setup Guide (PDF)](CDX-Demo-Tenant-Setup.pdf)**

---

## 🚀 Quick Setup Steps

### Step 1: Access CDX Portal

1. Go to [cdx.transform.microsoft.com](https://cdx.transform.microsoft.com)
2. Sign in with your Microsoft corporate credentials
3. Navigate to **My Environments**

### Step 2: Create a New Tenant

1. Click **Create Tenant**
2. Select the appropriate template:
   - **Microsoft 365 Enterprise** (recommended for Agentathons)
   - Ensure it includes **Power Platform** capabilities
3. Configure tenant settings:
   - Region: Select appropriate region (e.g., Europe for Spain events)
   - Duration: Set based on your event timeline (typically 30-90 days)

### Step 3: Enable Copilot Studio

1. Access the Power Platform Admin Center
2. Navigate to **Environments**
3. Create or configure an environment with:
   - Dataverse database enabled
   - Copilot Studio enabled

### Step 4: Configure Users

1. Create user accounts for all participants
2. Assign necessary licenses:
   - Microsoft 365 E5 or E3
   - Power Platform per user plan
   - Copilot Studio license

### Step 5: Prepare Sample Data

1. Upload sample documents to SharePoint for knowledge bases
2. Create sample Dataverse tables if needed
3. Configure any necessary connectors

---

## ⏱️ Timeline Recommendations

| When | Action |
|------|--------|
| **2 weeks before** | Create CDX tenant |
| **1 week before** | Add users and verify licenses |
| **3 days before** | Upload sample content, test access |
| **1 day before** | Final verification with all participants |

---

## ✅ Pre-Event Checklist

Before the Agentathon, verify:

- [ ] CDX tenant is active and accessible
- [ ] All participant accounts created
- [ ] Copilot Studio accessible at [copilotstudio.microsoft.com](https://copilotstudio.microsoft.com)
- [ ] Sample SharePoint site with documents ready
- [ ] Power Platform environment configured
- [ ] Test agent creation works

---

## ⚠️ Common Issues & Solutions

### Issue: Copilot Studio not available

**Solution**: Ensure the Power Platform environment has Copilot Studio enabled in the admin center.

### Issue: Users can't access the tenant

**Solution**: Verify licenses are assigned and users have completed first-time sign-in.

### Issue: Connectors not available

**Solution**: Check DLP (Data Loss Prevention) policies in the tenant.

### Issue: Tenant expired

**Solution**: Extend the tenant duration in CDX portal before expiration.

---

## 📞 Support

- **CDX Support**: Access help through the CDX portal
- **Internal Support**: Contact your local Microsoft team
- **Power Platform Issues**: [Power Platform Admin Center](https://admin.powerplatform.microsoft.com)

---

## 📚 Additional Resources

- [CDX Portal](https://cdx.transform.microsoft.com)
- [Power Platform Admin Documentation](https://learn.microsoft.com/en-us/power-platform/admin/)
- [Copilot Studio Documentation](https://learn.microsoft.com/en-us/microsoft-copilot-studio/)
