<properties
    pageTitle="Resolve Update Management issues with Azure Automation - Machines Not Listed"
    description="Resolve Update Management issues with Azure Automation"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32615227,32642182"
    resourceTags=""
    productPesIds="15607,15725"
    cloudEnvironments="public"
    articleId="bad97f5e-f660-4295-a360-df54b1784a65"
/>

# Resolve Update Management issues with Azure Automation - Machines not listed

This article will help with several kinds of issues relating to machines not showing up in the Azure Update Management solution.

## **Recommended Steps**

### **Machine was showing up, but disappeared**

* To prevent stale data, machines that have not reported in for 12 hours are not shown in Update Management

* Follow the steps in ["Machines don't show up under Update Management" ](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs) to check for the most recent reports from machines and common solutions

### **Update Agent Readiness doesn't show "ready"**

* For Azure VMs: run the troubleshooter from the "troubleshoot" link in the agent health report
* For non-Azure VMs, or if the troubleshooter doesn't work, see the ["Troubleshoot Offline"](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues#troubleshoot-offline) section of the Update Agent troubleshooter guide
* Consult the [Update Agent Troubleshooter document](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues#prerequisite-checks) for any checks that failed in order to remediate issues

### **The solution cannot be enabled on this VM because the VM already has the management agent..."**

* This error occurs when a machine is already enrolled into Update Management
* A common cause is when [Azure Security Center](https://docs.microsoft.com/azure/security-center/) already manages a machine.

### **Machine shows as "not assessed"**

Information can take a few minutes to propagate through Log Analytics, but if machines still show "not assessed", then:

* Follow the steps in ["Machines don't show up under Update Management" ](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs)

### **"No computers match the Update deployment target specification" error received**

* You may recieve this error if machines are offline when the deployment occurs. Follow the steps in ["Machines don't show up under Update Management" ](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs)
* Review the steps to creating a dynamic deployment, especially the note about permissions, in ["Using Dynamic Groups"](https://docs.microsoft.com/azure/automation/automation-update-management#using-dynamic-groups)

### **"You have requested to create an update configuration on a machine that is not registered for Update Management"**

* This issue is commonly related to Scope Configuration.
  * Option 1) [Update the scope configuration](https://docs.microsoft.com/azure/automation/automation-onboard-solutions-from-automation-account#scope-configuration) to add the desired machines, * Option 2) (Recommended) [Disable Scope Configuration](https://docs.microsoft.com/azure/automation/automation-onboard-solutions-from-automation-account#all-available-and-future-machines) and register all machines in the workspace for Update Management

## **Recommended Documents**

* [Troubleshoot issues using Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-management)
* [Troubleshoot issues onboarding Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/onboarding)
* [Understand the agent check results in Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues)
* [Update Management Overview](https://docs.microsoft.com/azure/automation/automation-update-management)
* [Update Management Tutorial](https://docs.microsoft.com/azure/automation/automation-tutorial-update-management)
* [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510)
