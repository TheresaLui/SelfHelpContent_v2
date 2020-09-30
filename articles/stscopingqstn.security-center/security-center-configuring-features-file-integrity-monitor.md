<properties
    pageTitle="Azure Security Center – Configuring Features – File Integrity Monitor"
    description="Azure Security Center – Configuring Features – File Integrity Monitor"
    authors="v-miegge"
    ms.author="kawilson"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32693232"
    resourceTags=""
    productPesIds="15947"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="1bd7162d-03e0-40a5-accb-7afcb30ccb4e"
	ownershipId="Azure_Security_Security_Center"
/>

# Azure Security Center – Configuring Features – File Integrity Monitor  

**Note:** FIM uses the Azure Change Tracking solution to track and identify changes in your environment. When File Integrity Monitoring is enabled, you have a Change Tracking resource of type Solution. For data collection frequency details, see [Change Tracking data collection details](https://docs.microsoft.com/azure/automation/automation-change-tracking#change-tracking-data-collection-details) for Azure Change Tracking.

## Azure Security Center File Integrity monitor Configuration failure

To resolve the configuration failure, open the relevant Log Analytics workspace and check the **Solution** section to see whether the following solutions are presented:

- Security
- Change tracking

If one of these two solutions are not enabled on the workspace solution list, go to **Security Center - File Integrity Monitoring**, and press **Enable** or **Upgrade**.

### Azure Security Center File Integrity monitor - FIM false report

To check if the false reporting is a UI issue or change tracking issue, you need to open Log Analytics workspace -> Logs and run this query:

    ConfigurationChange
    | where Computer == "Your_VM_Name"
    | where ConfigChangeType in("Files", "Registry")
    | order by TimeGenerated
    | render table

If you don't see the results in the workspace, contact our support.  

If results are returned, it means that the feature found a change, and the results did not appear in the FIM UI because of the 100 item view limitation. We only present the last 100 changes in the UI.

### Azure Security Center File Integrity monitor - FIM Workspace or other issue

File Integrity monitor uses the Azure Change Tracking solution to track and identify changes in your environment. When File Integrity Monitoring is enabled, a Change Tracking resource (Log Analytics workspace) is created in your subscription. If you remove this Change Tracking resource, File Integrity Monitoring feature will be disabled.

To resolve the configuration failure, you need to open the relevant Log Analytics workspace, and check the **Solution** section to see if the following two solutions are presented:

- Security
- Change tracking

If one of these two solutions are not enable on the workspace solution list, go to **Security Center - File Integrity Monitoring** and click **Upgrade** and **Enable**.

### Tips for troubleshooting

- File Integrity monitor works only on Azure VMs and on-premises machines
- The server that enables File Integrity monitoring must be monitored by Azure security center and the Azure Log Analytics agent must to be healthy
- Azure security center needs to be on standard pricing tier on the subscription level, and every User workspace to be used should also be in standard pricing tier (security solution be should install on it)
- File Integrity monitor does not work with PaaS services
- The File Integrity monitor UI in Azure portal only shows the last 100 changes. You should always run log analytics query to check if the changes appear in the user workspace.

## **Recommended Documents**

- [File Integrity Monitoring in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-file-integrity-monitoring)
- [File Integrity Monitoring Limitations](https://docs.microsoft.com/azure/automation/automation-change-tracking#change-tracking-data-collection-details)
- [ChangeTracking solution (FIM) regions availability](https://docs.microsoft.com/azure/automation/how-to/region-mappings)
- [Compare baselines using File Integrity Monitoring (FIM)](https://docs.microsoft.com/azure/security-center/security-center-file-integrity-monitoring-baselines)
### Azure Security Center Troubleshooting

- [Azure Security Center Troubleshooting Guide](https://docs.microsoft.com/azure/security-center/security-center-troubleshooting-guide)
- [Azure Security Center FAQ](https://docs.microsoft.com/azure/security-center/security-center-faq)

### How-To and Advisory Information
- [Latest Azure Security Center updates](https://docs.microsoft.com/azure/security-center/release-notes)
- [Azure Security Center Pricing Tiers](https://docs.microsoft.com/azure/security-center/security-center-pricing)
- [Permissions in Azure Security Center](https://docs.microsoft.com/azure/security-center/security-center-permissions)



