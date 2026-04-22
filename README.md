# Azure Cloud Security Monitoring with Activity Logs and Log Analytics

## Project Overview
I built this project to get hands-on experience with Azure cloud monitoring and to better understand how administrative activity can be tracked in a cloud environment.

For this lab, I worked with Azure Activity Logs, a Log Analytics workspace, diagnostic settings, and an action group. I created and deleted test resources, reviewed the resulting Activity Log events, and explored how Azure can centralize logs for monitoring and future investigation. The main goal was to understand the basic building blocks of cloud visibility in Azure and see how those pieces fit together in a practical workflow.

---

## Objective
The purpose of this project was to learn how Azure handles cloud monitoring from a practical security perspective. I wanted to understand:

- how administrative actions are recorded in Azure
- how to track resource changes such as updates and deletions
- how cloud logs can be sent to a centralized workspace
- how Azure monitoring components can be connected to notification workflows
- how to safely clean up cloud resources after a lab

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
- Basic monitoring workflow understanding
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

## What I Did

### 1. Reviewed Azure Activity Logs
I started by opening the subscription-level Azure Activity Log to understand what kinds of events were already being recorded. This helped me confirm that Azure was logging management activity and gave me a baseline before creating my own test events.

### 2. Created a Test Resource Group
To generate safe administrative activity, I created a test resource group named `rg-cloud-monitor-lab`. This gave me a simple way to produce real Azure events without making the lab too complex.

### 3. Monitored Administrative Activity
After creating the resource group, I went back to Azure Activity Log and reviewed the events related to it. I was able to see the operation name, event status, timestamps, and the user account that initiated the action. This helped me understand how Azure records routine management activity.

### 4. Deleted the Test Resource Group
Next, I deleted the same test resource group so I could observe how Azure logs a high-value administrative action like deletion. In the Activity Log, I could see the event progression and confirm that the delete action was captured clearly.

### 5. Created a Log Analytics Workspace
To take the project further, I created a Log Analytics workspace named `law-cloud-monitor-lab` in a separate resource group called `rg-log-analytics-lab`. This helped me understand how Azure supports centralized logging instead of relying only on the default Activity Log view.

### 6. Configured Diagnostic Settings
I then created a diagnostic setting named `ds-activitylog-to-law` to send Azure subscription Activity Logs to the Log Analytics workspace. This was an important step because it showed how cloud logs can be forwarded into a central place for monitoring and later analysis.

### 7. Explored the Logs Workspace
After setting up the diagnostic configuration, I opened the Log Analytics workspace and reviewed the Logs page. This helped me understand how the workspace would be used for centralized visibility and future investigation.

### 8. Created an Action Group
I also created an Azure Monitor action group named `ag-cloud-monitor-lab` with an email notification. My goal here was to understand how monitoring in Azure can connect to notification workflows and what the alerting side of the monitoring process looks like.

### 9. Cleaned Up Resources
After finishing the lab and capturing the evidence I needed, I deleted the monitoring resource group and removed the diagnostic setting. I wanted to make sure the lab was cleaned up properly and that no unnecessary cloud resources were left running.

---

## Key Takeaways

### Azure clearly records management activity
One of the biggest things I learned from this project is that Azure Activity Log provides useful visibility into administrative actions. I was able to see updates, deletions, timestamps, success status, and user attribution in a straightforward way.

### User attribution matters
The logs clearly showed which account performed the action. From a security point of view, that is important because it helps with accountability and makes it easier to review whether an action was expected or suspicious.

### Centralized logging is an important next step
Using diagnostic settings to send Activity Logs to a Log Analytics workspace helped me understand how organizations move from basic portal-level visibility to more centralized monitoring.

### Cloud monitoring involves multiple connected components
This project showed me that Azure monitoring is not just one screen or one log source. It involves Activity Logs, workspaces, diagnostic settings, and action or notification components that work together.

---

## Why This Matters for Security
This project is useful from a security perspective because cloud environments depend heavily on visibility. If a resource is created, changed, or deleted, security teams need to know:

- what happened
- when it happened
- who initiated it
- whether the activity looks normal or unexpected

Even though this was a beginner project, it helped me build a foundation in how cloud monitoring supports investigation, auditability, and operational awareness.

---

## Challenges I Faced
A few parts of the lab were not completely straightforward. Some Activity Log events took time to appear, so I had to refresh the log view and adjust the time range. I also ran into Azure region restrictions while creating the Log Analytics workspace, which meant I had to try an allowed region before the deployment worked. On the monitoring side, I saw that some alerting paths became broader and more complex than I wanted for a small lab, so I kept the project focused on safe and practical cloud monitoring tasks.

---

## What I Learned
This project helped me understand:

- how Azure records administrative activity
- how to track resource lifecycle actions like creation and deletion
- how to review operation names, status, timestamps, and user attribution
- how to create and use a Log Analytics workspace
- how to configure diagnostic settings for centralized log collection
- how Azure monitoring can connect to notification workflows through action groups
- why cleanup is important after working in cloud environments

---

## Future Improvements
If I extend this project later, I would like to:

- analyze ingested logs directly in Log Analytics after more data is available
- create more targeted Azure Monitor alert rules
- work with Microsoft Entra sign-in or audit logs
- simulate additional security-focused cloud changes
- explore Microsoft Sentinel as a next step for larger-scale monitoring

---

## Conclusion
This project gave me practical exposure to Azure cloud monitoring and helped me understand how administrative activity is recorded, forwarded, and reviewed. It strengthened my understanding of cloud audit trails, centralized logging, and the monitoring workflow in Azure. More importantly, it gave me a hands-on way to connect cloud administration activity with security visibility.

---

## Author
**Abhishek Raghuraman**

GitHub: [https://github.com/Abby879](https://github.com/Abby879)
