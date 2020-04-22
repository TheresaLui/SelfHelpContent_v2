<properties
    pageTitle="Azure Automation - Update Management - Enabling Update Management"
    description="Resolve Update Management issues with Azure Automation"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32599864"
    resourceTags=""
    productPesIds="15607,15725"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="26220297-1137-4a58-b966-f1572984c85b"
	ownershipId="Compute_Automation"
/>

# I enabled Update Management but it says "this can take a few minutes"

This article will help with several kinds of issues relating to onboarding the Azure Update Management solution.

## **Recommended Steps**

First, try running the Update Agent Troubleshooter ([Windows](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues), [Linux](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues-linux)) which addresses many common issues. 

### **Machine isn't onboarding after waiting**

* Refer to [the "Components enabled but not working" section of the Update Management Troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#components-enabled-not-working)

### **Update Agent Readiness doesn't show "ready"**

* For Azure VMs: run the troubleshooter from the "troubleshoot" link in the agent health report
* For non-Azure VMs, or if the troubleshooter doesn't work, see the ["Troubleshoot Offline"](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues#troubleshoot-offline) section of the Update Agent troubleshooter guide
* Consult the [Update Agent Troubleshooter document](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues#prerequisite-checks) for any checks that failed in order to remediate issues

### **The solution cannot be enabled on this VM because the VM already has the management agent..."**

* This error occurs when a machine is already enrolled into Update Management
* A common cause is when [Azure Security Center](https://docs.microsoft.com/azure/security-center/) already manages a machine

### **Machine shows as "not assessed"**

Information can take a few minutes to propagate through Log Analytics, but if machines still show "not assessed", then:

* Follow the troubleshooting guide for ["Machines don't show up in the portal"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs)
* If you see an error code like "Exception from HRESULT 0x...", follow the troubleshooting guide for ["Machine shows as Not Assessed and shows an HResult exception"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#hresult)

## **Recommended Documents**

* [Troubleshoot issues using Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-management)
* [Troubleshoot issues onboarding Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/onboarding)
* [Understand the agent check results in Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues)
* [Update Management Overview](https://docs.microsoft.com/azure/automation/automation-update-management)
* [Update Management Tutorial](https://docs.microsoft.com/azure/automation/automation-tutorial-update-management)
* [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510)
