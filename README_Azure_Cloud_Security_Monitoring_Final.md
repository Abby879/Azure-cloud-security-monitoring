# Azure Cloud Security Monitoring with Activity Logs and Log Analytics

## Project Overview
This project demonstrates a beginner-level Azure cloud security monitoring lab focused on administrative activity logging, centralized log collection, and basic monitoring workflow setup.

The goal of the project was to understand how Azure records management actions, how those logs can be collected in a Log Analytics workspace, and how cloud activity can be reviewed from a security monitoring perspective.

In this lab, I created and deleted a test Azure resource group, reviewed the related Activity Log events, configured diagnostic settings to forward Activity Logs to a Log Analytics workspace, and created an action group to understand how Azure monitoring workflows can connect to notifications.

---

## Objective
The objective of this project was to gain hands-on experience with Azure cloud monitoring by:

- creating and deleting test resources in Azure
- reviewing Azure Activity Log entries
- tracking administrative events such as updates and deletions
- understanding user attribution, status, and timestamps in cloud logs
- configuring diagnostic settings to export Activity Logs to Log Analytics
- exploring the setup of monitoring and notification components in Azure

---

## Tools Used
- Microsoft Azure Portal
- Azure Activity Log
- Azure Resource Groups
- Log Analytics Workspace
- Azure Monitor Diagnostic Settings
- Azure Monitor Action Groups

---

## Skills Demonstrated
- Cloud security monitoring
- Azure Activity Log analysis
- Administrative event tracking
- Audit trail review
- Resource lifecycle monitoring
- Centralized log collection
- Basic monitoring workflow setup
- Documentation and evidence collection

---

## Environment
- **Platform:** Microsoft Azure
- **Subscription:** Azure for Students
- **Primary Test Resource Group:** `rg-cloud-monitor-lab`
- **Monitoring Resource Group:** `rg-log-analytics-lab`
- **Log Analytics Workspace:** `law-cloud-monitor-lab`
- **Action Group:** `ag-cloud-monitor-lab`

---

## Project Steps

### 1. Reviewed Initial Azure Activity Logs
I first opened Azure Activity Log at the subscription level to confirm that Azure was recording management events. Initial events included subscription creation and automatic policy-related activity.

### 2. Created a Test Resource Group
I created a resource group named `rg-cloud-monitor-lab` to generate a safe administrative event in the Azure environment.

### 3. Reviewed Resource Group Activity
After creating the resource group, I reviewed Azure Activity Logs and observed administrative events related to the resource group, including update operations, success status, and the initiating user account.

### 4. Deleted the Test Resource Group
I deleted the same resource group and captured the related Azure Activity Log events. The log showed the event progression and confirmed that Azure recorded the delete action successfully.

### 5. Created a Log Analytics Workspace
To strengthen the project, I created a Log Analytics workspace named `law-cloud-monitor-lab` in a separate resource group called `rg-log-analytics-lab`.

### 6. Configured Diagnostic Settings
I configured a diagnostic setting named `ds-activitylog-to-law` to send Azure subscription Activity Logs to the Log Analytics workspace.

### 7. Reviewed the Logs Workspace
I opened the Log Analytics workspace and verified that the workspace and logs page were available for centralized monitoring.

### 8. Created an Action Group
I created an Azure Monitor action group named `ag-cloud-monitor-lab` with an email notification to understand how Azure monitoring workflows can be connected to notification actions.

### 9. Cleaned Up Resources
After collecting screenshots and documenting the project, I deleted the monitoring resource group and removed the diagnostic setting to stop further log export.

---

## Key Findings

### Finding 1: Azure records administrative cloud activity clearly
Azure Activity Log captured management actions such as resource group updates and deletions, including status, time, and the initiating account.

### Finding 2: Cloud audit trails support accountability
The logs clearly showed who performed an action and whether the action succeeded. This is important for security monitoring, investigation, and audit review.

### Finding 3: Centralized log collection is possible through diagnostic settings
By using diagnostic settings, Azure Activity Logs can be forwarded to a Log Analytics workspace for centralized log collection and future analysis.

### Finding 4: Monitoring workflows involve multiple components
A complete monitoring setup in Azure can include Activity Logs, a Log Analytics workspace, diagnostic settings, and action groups for notification workflows.

---

## Security Relevance
This project is relevant to cybersecurity because cloud environments depend heavily on visibility into administrative actions. Monitoring cloud logs helps security teams:

- track resource changes
- identify unexpected administrative actions
- verify who performed changes
- support incident response and audit investigations
- understand cloud monitoring architecture

Even though this was a beginner lab, it reflects the foundation of how cloud audit logging and monitoring workflows work in Azure.

---

## Screenshots
Store the screenshots in a `screenshots` folder and reference them in this order:

1. `01-resource-group-created.png`
2. `02-resource-group-activity-log.png`
3. `03-delete-resource-group-event.png`
4. `04-delete-event-details.png`
5. `05-log-analytics-workspace-created.png`
6. `06-log-analytics-workspace-overview.png`
7. `07-diagnostic-setting.png`
8. `08-log-analytics-logs-page.png`

---

## Challenges Faced
One challenge during the project was that some Azure Activity Log events did not appear immediately, which required refreshing the Activity Log and adjusting the time range.

Another challenge was that certain Azure monitoring and alerting configurations became broader and more complex than expected, so the project was kept focused on a safe, low-usage cloud monitoring setup.

Subscription region restrictions also affected workspace deployment, so I had to test an allowed region before successfully creating the Log Analytics workspace.

---

## What I Learned
From this project, I learned:

- how Azure records administrative events in Activity Log
- how to track resource lifecycle actions such as creation and deletion
- how to identify status, timestamps, and initiating users in logs
- how to create a Log Analytics workspace
- how to configure diagnostic settings for centralized log collection
- how Azure monitoring workflows can connect to notification components like action groups
- why cleanup is important after completing cloud labs

---

## Future Improvements
This project could be extended in the future by:

- analyzing logs directly in Log Analytics after ingestion completes
- creating more targeted Azure Monitor alert rules
- integrating Microsoft Entra sign-in or audit logs
- simulating more security-focused configuration changes
- exploring Microsoft Sentinel for larger-scale monitoring

---

## Conclusion
This project gave me practical exposure to Azure cloud monitoring and helped me understand how administrative actions are captured, exported, and reviewed. It strengthened my understanding of cloud audit trails, centralized logging, and the basic building blocks of Azure monitoring workflows.

---

## Author
**Abhishek Raghuraman**

GitHub: [https://github.com/Abby879](https://github.com/Abby879)
