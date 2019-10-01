<properties
    pageTitle="Resolve Update Management issues with Azure Automation"
    description="Resolve Update Management issues with Azure Automation"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32642184,32599924,32642191,32612529"
    resourceTags=""
    productPesIds="15607,15725"
    cloudEnvironments="public"
    articleId="6a3512a4-53ee-48c2-a748-f8cff1d4bb04"
/>

# Resolve Update Management issues with Azure Automation

This article will help with several kinds of issues relating to onboarding and using the Azure Update Management solution. For general questions about Update Management scenarios, see [Update Management Overview](https://docs.microsoft.com/azure/automation/automation-update-management)

## **Recommended Steps**

First, try running the Update Agent Troubleshooter ([Windows](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues), [Linux](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues-linux)) which addresses many common issues. 

### **Desired automation account, region, or Log Analytics workspace is greyed out**

* Only certain regions are supported for linking Log Analytics and Automation Accounts, which is required for Update Management. See the ["Workspace Mappings"](https://docs.microsoft.com/azure/automation/how-to/region-mappings) document for the full list of supported regions.

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

* Follow the steps in ["Machines don't show up under Update Management" ](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs)

### **Remove machine from Update Management**

* To unenroll a machine from Update Management, follow the instructions at ["Remove a VM from Update Management"](https://docs.microsoft.com/azure/automation/automation-update-management#remove-a-vm-for-update-management)

### **Machines don't install updates**

* Try running updates directly on the machine. If the machine cannot update, consult the [list of potential errors in the troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#hresult).
* If updates run locally, try removing and reinstalling the agent on the machine by following the instructions at ["Remove a VM from Update Management"](https://docs.microsoft.com/azure/automation/automation-update-management#remove-a-vm-for-update-management).

### **"No computers match the Update deployment target specification" error received**

* You may see this error if machines are offline when the deployment occurs. Follow the steps in ["Machines don't show up under Update Management" ](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs)
* Review the steps to creating a dynamic deployment, especially the note about permissions, in ["Using Dynamic Groups"](https://docs.microsoft.com/azure/automation/automation-update-management#using-dynamic-groups)

### **"You have requested to create an update configuration on a machine that is not registered for Update Management"**

* This issue is commonly related to Scope Configuration:

  * Option 1) [Update the scope configuration](https://docs.microsoft.com/azure/automation/automation-onboard-solutions-from-automation-account#scope-configuration) to add the desired machines
  * Option 2) (Recommended) [Disable Scope Configuration](https://docs.microsoft.com/azure/automation/automation-onboard-solutions-from-automation-account#all-available-and-future-machines) and register all machines in the workspace for Update Management

### **Machines update without an update deployment**

* If machines are receiving updates without an update deployment, please see the note under ["Install Updates" of the Update Management overview document](https://docs.microsoft.com/azure/automation/automation-update-management#install-updates).

### **I know updates are available, but they don't show as needed on my machines**

* This often happens if machines are configured to get updates from WSUS/SCCM, but WSUS/SCCM have not approved the updates.
* You can check if machines are configured for WSUS/SCCM by [cross-referencing the "UseWUServer" registry key to the registry keys in the "Configuring Automatic Updates by Editing the Registry" section of this document](https://support.microsoft.com/help/328010/how-to-configure-automatic-updates-by-using-group-policy-or-registry-s)

### **Updates show as installed, but I can't find them on my machine**

* Updates are often superseded by other updates. For more information, see ["Update is superseded" in the Windows Update Troubleshooting guide](https://docs.microsoft.com/windows/deployment/update/windows-update-troubleshooting#the-update-is-not-applicable-to-your-computer)

### **Updating machines across different tenants**

* If you receive an error message saying "The current tenant is not authorized to access the linked subscription", please use [the workaround here](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#multi-tenant).


## **Recommended Documents**

* [Troubleshoot issues using Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-management)
* [Troubleshoot issues onboarding Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/onboarding)
* [Understand the agent check results in Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues)
* [Update Management Overview](https://docs.microsoft.com/azure/automation/automation-update-management)
* [Update Management Tutorial](https://docs.microsoft.com/azure/automation/automation-tutorial-update-management)
* [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510)
