<properties
    pageTitle="Resolve Update Management issues with Azure Automation - Machines Not Listed"
    description="Resolve Update Management issues with Azure Automation"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder="103"
    selfHelpType="generic"
    supportTopicIds="32615227,32642182"
    resourceTags=""
    productPesIds="15607,15725"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="bad97f5e-f660-4295-a360-df54b1784a65"
	ownershipId="Compute_Automation"
/>

# Resolve Update Management issues with Azure Automation - Machines not listed

This article will help with several kinds of issues relating to machines not showing up in the Azure Update Management solution.

## **Recommended Steps**

The Update Agent Troubleshooter ([Windows](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues), [Linux](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues-linux)) will detect common issues such as restrictive firewalls, missing prerequisites, or misconfigured registry keys. 

### **Machines not showing up in the portal**

* Follow the steps in ["Machines don't show up under Update Management" ](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs) for instructions on how to:
  
  * Make sure that your machine is reporting to the correct workspace
  * Make sure Scope Configuration is not preventing your machine from enrolling in Update Management
  * Check your Log Analytics configuration to ensure log ingestion is working
  
### **Update Agent Readiness shows "Not Configured" or "Not Assessed"**

* Follow the steps in ["Machines don't show up under Update Management" ](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs) to check for the most recent reports from machines and common solutions
* If you see an error code like "Exception from HRESULT 0x...", follow the troubleshooting guide for ["Machine shows as Not Assessed and shows an HResult exception"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#hresult)

  * This error commonly indicates an inaccessible WSUS server has been configured, or Windows Update is not reachable on the network

## **Recommended Documents**

* [Update Management Overview - Supported Clients, Permissions and Network Requirements](https://docs.microsoft.com/azure/automation/automation-update-management)
* [Update Management Tutorial - Manage Updates for Multiple VMs](https://docs.microsoft.com/azure/automation/manage-update-multi)
* [Configure Windows Update Client Settings for Update Management](https://docs.microsoft.com/azure/automation/automation-configure-windows-update)
