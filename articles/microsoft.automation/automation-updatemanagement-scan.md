<properties
    pageTitle="Resolve Update Management issues with Azure Automation - Scan and Deploy"
    description="Resolve Update Management issues with Azure Automation"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32615228, 32642187"
    resourceTags=""
    productPesIds="15607,15725"
    cloudEnvironments="public"
    articleId="754ca972-a640-407c-8f78-a0836b393a9d"
/>

# Resolve Update Management issues with Azure Automation - Scanning for and Deploying Updates

This article will help with several kinds of issues relating to using the Azure Update Management solution.

## **Recommended Steps**

### **I know updates are available, but they don't show as needed on my machines**

* This often happens if machines are configured to get updates from WSUS/SCCM, but WSUS/SCCM have not approved the updates.
* You can check if machines are configured for WSUS/SCCM by [cross-referencing the "UseWUServer" registry key to the registry keys in the "Configuring Automatic Updates by Editing the Registry" section of this document](https://support.microsoft.com/help/328010/how-to-configure-automatic-updates-by-using-group-policy-or-registry-s)

### **Updates show as installed, but I can't find them on my machine**

* Updates are often superceded by other updates. For more information, see ["Update is superseded" in the Windows Update Troubleshooting guide](https://docs.microsoft.com/windows/deployment/update/windows-update-troubleshooting#the-update-is-not-applicable-to-your-computer)


### **Machine shows as "not assessed"**

Information can take a few minutes to propagate through Log Analytics, but if machines still show "not assessed", then:

* Check for a [Log Analytics heartbeat](https://docs.microsoft.com/azure/automation/automation-update-management#confirm-that-non-azure-machines-are-onboarded)
* If there is no heartbeat, check the [Solution Scoping](https://docs.microsoft.com/azure/automation/automation-onboard-solutions-from-automation-account#scope-configuration) is correct
* If there is a heartbeat, follow the steps in the [Data not Showing in Log Analytics section of the Update Management troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs)
* If there is an error code listed, see the [list of potential errors in the troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#hresult).


### **Machines don't install updates**

* Try running updates directly on the machine. If the machine cannot update, consult the [list of potential errors in the troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#hresult).
* If updates run locally, try removing and reinstalling the agent on the machine by following the instructions at ["Remove a VM from Update Management"](https://docs.microsoft.com/azure/automation/automation-update-management#remove-a-vm-for-update-management).

### Installing updates by classification on Linux

* Deploying updates to Linux by classification ("Critical and security updates") has important caveats, especially for CentOS. These [limitations are documented on the Update Management overview page](https://docs.microsoft.com/azure/automation/automation-update-management#linux-2)

### **Machines update without an update deployment**

* If machines are receiving updates without an update deployment, please see the note under ["Install Updates" of the Update Management overview document](https://docs.microsoft.com/azure/automation/automation-update-management#install-updates).

### **Updating machines across different tenants**

* If you receive an error message saying "The current tenant is not authorized to access the linked subscription", please use [the workaround here](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#multi-tenant)

### **Update Agent Readiness doesn't show "ready"**

* For Azure VMs: run the troubleshooter from the "troubleshoot" link in the agent health report
* For non-Azure VMs, or if the troubleshooter doesn't work, see the ["Troubleshoot Offline"](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues#troubleshoot-offline) section of the Update Agent troubleshooter guide
* Consult the [Update Agent Troubleshooter document](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues#prerequisite-checks) for any checks that failed in order to remediate issues


## **Recommended Documents**

* [Troubleshoot issues using Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-management)
* [Troubleshoot issues onboarding Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/onboarding)
* [Understand the agent check results in Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues)
* [Update Management Overview](https://docs.microsoft.com/azure/automation/automation-update-management)
* [Update Management Tutorial](https://docs.microsoft.com/azure/automation/automation-tutorial-update-management)
* [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510)
