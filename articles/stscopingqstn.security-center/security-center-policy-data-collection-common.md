<properties
    pageTitle="Data Collection Common Solutions"
    description="Data Collection Common Solutions"
    service=""
    resource=""
    authors="TobyTu"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32680780"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="a15f057d-8uj6-4b77-a98a-dfaf3843dc2f"
	ownershipId="Azure_Security_Security_Center"
/>

# Data Collection Common Solutions

Data collected by Security Center is stored in Log Analytics workspace(s). You can select to have data collected from Azure VMs stored in workspace created by Security Center or in an existing workspace you created.

**Tips for Workspace**

- Workspace configuration is set per subscription, and many subscriptions may use the same workspace
- When you select a workspace in which to store your data, all the workspace across all your subscriptions are available
- Cross-subscription workspace selection allows you to collect data from virtual machines running in different subscriptions and store it in the workspace of your choice. This selection is useful if you are using a centralized workspace in your organization and want to use it for security data collection. For more information on how to manage workspace, see [Manage workspace access](https://docs.microsoft.com/azure/log-analytics/log-analytics-manage-access)

**Data Collection Tier**

Selecting a data collection tier in Azure Security Center will only affect the storage of security events in your Log Analytics workspace. The Log Analytics agent will still collect and analyze the security events required for Azure Security Center's threat detections, regardless of which tier of security events you choose to store in your Log Analytics workspace (if any). Choosing to store security events in your workspace will enable investigation, search, and auditing of those events in your workspace.

## **Recommended Documents**

- [Azure Security Center Data Collection Workspace Configuration](https://docs.microsoft.com/azure/security-center/security-center-enable-data-collection#workspace-configuration)
- [Azure Security Center Data Collection Cross Subscription Workspace Selection](https://docs.microsoft.com/azure/security-center/security-center-enable-data-collection#cross-subscription-workspace-selection)
- [Manage log data and workspace in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/manage-access)

**Troubleshooting**

- [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)

**FAQ**

- [Azure Security Center FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)
