<properties
    pageTitle="Azure Automation - Update Management"
    description="Azure Automation - Update Management"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32599861,32599924,32599864,32599868,32599903,32599925,32599936,32599937,32615226,32615227,32615229,32615228,32612529"
    resourceTags=""
    productPesIds="15607,15725"
    cloudEnvironments="public"
	articleId="6a3512a4-53ee-48c2-a748-f8cff1d4bb04"
/>
# Azure Automation - Update Management
This article will help with several kinds of issues relating to onboarding and using the Azure Update Management solution.

## **Recommended Steps**

### **Machine isn't onboarding after waiting 15 minutes**

* Refer to the ["Components enabled but not working" section of the Update Management Troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#components-enabled-not-working)

### **Update Agent Readiness doesn't show "ready"**

* For Azure VMs: run the troubleshooter from the "troubleshoot" link in the agent health report
* For non-Azure VMs, or if the troubleshooter doesn't work, see the ["Troubleshoot Offline"](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues#troubleshoot-offline) section of the Update Agent troubleshooter guide
* Consult the [Update Agent Troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues#prerequisite-checks) for any checks that failed in order to remediate issues

### **Machine shows as "not assessed"**

Information can take a few minutes to propagate through Log Analytics, but if machines still show "not assessed":

* Check for a [Log Analytics heartbeat](https://docs.microsoft.com/azure/automation/automation-update-management#confirm-that-non-azure-machines-are-onboarded)
* If there is no heartbeat, check the [Solution Scoping](https://docs.microsoft.com/azure/automation/automation-onboard-solutions-from-automation-account#scope-configuration) is correct
* If there is a heartbeat, follow the steps in the [Data not Showing in Log Analytics section of the Update Management troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs)


## **Recommended Documents**

* [Troubleshoot issues using Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-management)
* [Troubleshoot issues onboarding Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/onboarding)
* [Understand the agent check results in Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues)
* [Update Management Overview](https://docs.microsoft.com/azure/automation/automation-update-management)
* [Update Management Tutorial](https://docs.microsoft.com/azure/automation/automation-tutorial-update-management)
* [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510)
