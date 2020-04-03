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
    cloudEnvironments="public, Fairfax"
    articleId="bad97f5e-f660-4295-a360-df54b1784a65"
	ownershipId="Compute_Automation"
/>

# Resolve Update Management issues with Azure Automation - Machines not listed

This article will help with several kinds of issues relating to machines not showing up in the Azure Update Management solution.

## **Recommended Steps**

First, try running the Update Agent Troubleshooter ([Windows](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues), [Linux](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues-linux)) which addresses many common issues. 

### **Machines not showing up in the portal**

* To prevent stale data, machines that have not reported in for 12 hours are not shown in Update Management
* Follow the steps in ["Machines don't show up under Update Management" ](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs) to check for the most recent reports from machines and common solutions

### **Update Agent Readiness shows "Not Configured" or "Not Assessed"**

* Follow the steps in ["Machines don't show up under Update Management" ](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs) to check for the most recent reports from machines and common solutions
* If you see an error code like "Exception from HRESULT 0x...", follow the troubleshooting guide for ["Machine shows as Not Assessed and shows an HResult exception"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#hresult)


### **The solution cannot be enabled on this VM because the VM already has the management agent..."**

* This error occurs when a machine is already enrolled into Update Management
* A common cause is when [Azure Security Center](https://docs.microsoft.com/azure/security-center/) already manages a machine


### **"No computers match the Update deployment target specification" error received**

* You may see this error if machines are offline when the deployment occurs. Follow the steps in ["Machines don't show up under Update Management" ](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs).
* Review the steps to creating a dynamic deployment, especially the note about permissions, in ["Use Dynamic Groups"](https://docs.microsoft.com/azure/automation/automation-update-management-groups)

### **"You have requested to create an update configuration on a machine that is not registered for Update Management"**

* This issue is commonly related to Scope Configuration:

  * Option 1) [Update the scope configuration](https://docs.microsoft.com/azure/automation/automation-onboard-solutions-from-automation-account#scope-configuration) to add the desired machines
  * Option 2) (Recommended) [Disable Scope Configuration](https://docs.microsoft.com/azure/automation/automation-onboard-solutions-from-automation-account#all-available-and-future-machines) and register all machines in the workspace for Update Management


### **Using Update Management with SCCM/SCOM**

 * Refer to ["Integrate System Center with Update Management"](https://docs.microsoft.com/azure/automation/oms-solution-updatemgmt-sccmintegration)

## **Recommended Documents**

* [Troubleshoot issues using Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-management)
* [Troubleshoot issues onboarding Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/onboarding)
* [Understand the agent check results in Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues)
* [Update Management Overview](https://docs.microsoft.com/azure/automation/automation-update-management)
* [Update Management Tutorial](https://docs.microsoft.com/azure/automation/automation-tutorial-update-management)
* [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510)
