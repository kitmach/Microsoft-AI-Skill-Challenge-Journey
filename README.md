# 🚀 Microsoft AI Skills Challenge - Learning Journey

Welcome to my learning journal for the [Microsoft AI Skills Challenge](https://aka.ms/aiskillschallenge)! This repository tracks my progress, key learnings, and hands-on projects using Azure AI Services.

---

## 📅 Challenge Dates
**Start Date:** May 13, 2025  
**End Date:** May 29, 2025

---

## 📦 Migration Essentials for Azure and AI Workloads

This section documents my work through the migration path of the challenge, including hands-on deployment, testing, and teardown of Azure-hosted applications.

📁 [View Project Folder](./projects/migration-essentials-azure-ai/)

### 🔧 Completed Labs & Actions

- Migrated a Go-based web app and PostgreSQL database to Azure VM + Azure Database for PostgreSQL (Flexible Server)
- Exposed the app on `http://<vm-ip>:8080` and verified via curl/browser
- Handled real-time web requests and viewed structured logs
- Created NSG and ASG rules to protect VM access
- Explored authentication using **Managed Identity + Microsoft Entra ID**
- Cleaned up all resources using `az deployment group create --mode Complete`

### 🔐 Security Learnings

- Prefer **Managed Identity** for secure database connections (no secrets in code)
- Limit VM access using **NSG rules** instead of exposing public ports
- Monitor logs for abnormal traffic (e.g., `/cgi-bin/luci/...` exploit attempts)
- Always delete unused resources to reduce cost and attack surface

### 🛠️ Cleanup Command Used

```powershell
az deployment group create `
  --resource-group 240900-linux-postgres `
  --template-file deploy/empty.bicep `
  --mode Complete
✅ Learning Path Progress
Learning Path	Status
Get started with Azure AI	✅ Completed
Use Azure AI services to build intelligence into your apps	⬜ In Progress
Develop machine learning models with Azure Machine Learning	⬜ Not Started
Use natural language processing with Azure OpenAI Service	⬜ Not Started
Build bots and AI-powered apps with Azure AI Studio	⬜ Not Started

🧠 Key Learnings So Far
Configuring Azure Cognitive Services via single-service resources

Integrating APIs like Anomaly Detector and OpenAI in Python

Using Azure Monitor and Logic Apps for workflow automation

Understanding cost management and resource planning in Azure

📚 My Microsoft Learn Profile
🔗 View my Microsoft Learn Profile

🏅 Badges & Achievements
You can view my earned badges and certifications here:
🔗 https://learn.microsoft.com/en-us/users/han-1434/achievements

💬 Feedback & Collaboration
Feel free to ⭐ this repo if you're following a similar journey.
Open an issue or fork the project if you'd like to collaborate or discuss Azure AI use cases!
