<properties
    pageTitle="Resolve Update Management issues with Azure Automation"
    description="Resolve Update Management issues with Azure Automation"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32599861,32599864,32615228,32599903,32615227,32599924,32615229,32599936,32599937"
    resourceTags=""
    productPesIds="15607,15725"
    cloudEnvironments="public"
    articleId="6a3512a4-53ee-48c2-a748-f8cff1d4bb04"
/>

# Resolve Update Management issues with Azure Automation

This article will help with several kinds of issues relating to onboarding and using the Azure Update Management solution.

## **Recommended Steps**

### **Machine isn't onboarding after waiting 15 minutes**

* Refer to [the "Components enabled but not working" section of the Update Management Troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#components-enabled-not-working)

### **Update Agent Readiness doesn't show "ready"**

* For Azure VMs: run the troubleshooter from the "troubleshoot" link in the agent health report
* For non-Azure VMs, or if the troubleshooter doesn't work, see the ["Troubleshoot Offline"](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues#troubleshoot-offline) section of the Update Agent troubleshooter guide
* Consult the [Update Agent Troubleshooter document](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues#prerequisite-checks) for any checks that failed in order to remediate issues

### **The solution cannot be enabled on this VM because the VM already has the management agent..."**

* This error occurs when a machine is already enrolled into Update Management
* A common cause is when [Azure Security Center](https://docs.microsoft.com/azure/security-center/) already manages a machine.

### **Machine shows as "not assessed"**

Information can take a few minutes to propagate through Log Analytics, but if machines still show "not assessed", then:

* Check for a [Log Analytics heartbeat](https://docs.microsoft.com/azure/automation/automation-update-management#confirm-that-non-azure-machines-are-onboarded)
* If there is no heartbeat, check the [Solution Scoping](https://docs.microsoft.com/azure/automation/automation-onboard-solutions-from-automation-account#scope-configuration) is correct
* If there is a heartbeat, follow the steps in the [Data not Showing in Log Analytics section of the Update Management troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs)
* If there is an error code listed, see the [list of potential errors in the troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#hresult).

### **Remove machine from Update Management**

* To unenroll a machine from Update Management, follow the instructions at ["Remove a VM from Update Management"](https://docs.microsoft.com/azure/automation/automation-update-management#remove-a-vm-for-update-management)

### **Machines don't install updates**

* Try running updates directly on the machine. If the machine cannot update, consult the [list of potential errors in the troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#hresult).
* If updates run locally, try removing and reinstalling the agent on the machine by following the instructions at ["Remove a VM from Update Management"](https://docs.microsoft.com/azure/automation/automation-update-management#remove-a-vm-for-update-management).

### **Machines update without an update deployment**

* If machines are receiving updates without an update deployment, please see the note under ["Install Updates" of the Update Management overview document](https://docs.microsoft.com/azure/automation/automation-update-management#install-updates).

### **Updating machines across different tenants**

* If you receive an error message saying "The current tenant is not authorized to access the linked subscription", please use [the workaround here](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#multi-tenant)


## **Recommended Documents**

* [Troubleshoot issues using Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-management)
* [Troubleshoot issues onboarding Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/onboarding)
* [Understand the agent check results in Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues)
* [Update Management Overview](https://docs.microsoft.com/azure/automation/automation-update-management)
* [Update Management Tutorial](https://docs.microsoft.com/azure/automation/automation-tutorial-update-management)
* [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510)
