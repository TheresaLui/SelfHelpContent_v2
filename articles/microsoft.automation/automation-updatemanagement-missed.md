<properties
    pageTitle="Resolve Update Management issues with Azure Automation - Missed Updates"
    description="Resolve Update Management issues with Azure Automation"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32599937"
    resourceTags=""
    productPesIds="15607,15725"
    cloudEnvironments="public, Fairfax"
    articleId="7784e652-9ef4-42a9-ac42-e13c9d604aba"
	ownershipId="Compute_Automation"
/>

# Resolve Update Management issues with Azure Automation - Update Deployment Didn't Install

This article will help for issues where machines are enrolled in Update Management, but an Update Deployment failed to install some or all updates.

## **Recommended Steps**

### **Update run returns status "Failed"**

* Follow the troubleshooting guide for ["Update run returns status 'Failed'"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#scenario-update-run-returns-status-failed)

### **"Exception: Job was suspended"**

* Run [the Update Agent troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues#troubleshoot-offline)

### **I know updates are available, but they don't show as needed on my machines**

* This often happens if machines are configured to get updates from WSUS/SCCM, but WSUS/SCCM have not approved the updates
* [Check if machines are configured for WSUS/SCCM](https://support.microsoft.com/help/328010/how-to-configure-automatic-updates-by-using-group-policy-or-registry-s)
* If machines are configured for WSUS then [run the Client Diagnostics tool](https://docs.microsoft.com/windows-server/administration/windows-server-update-services/manage/wsus-tools) 

### **I can't find or install a specific update**

* Updates are often [superseded by other updates](https://docs.microsoft.com/windows/deployment/update/windows-update-troubleshooting#the-update-is-not-applicable-to-your-computer). The superseded update will no longer appear in Update Management, even if the [Inclusion feature](https://docs.microsoft.com/azure/automation/automation-tutorial-update-management#schedule-an-update-deployment) is used to specify the KB number. 

### **Installing updates by classification on Linux**

* Deploying updates to Linux by classification ("Critical and security updates") has important caveats, especially for CentOS. These [limitations are documented on the Update Management overview page](https://docs.microsoft.com/azure/automation/automation-update-management#linux-2).

### **KB2267602 is consistently shown as missing**

* KB2267602 is the [Windows Defender definition update](https://www.microsoft.com/wdsi/definitions). It is updated daily.

### **Update Agent Readiness doesn't show "ready"**

* For Azure VMs: run the troubleshooter from the "troubleshoot" link in the agent health report
* For non-Azure VMs, or if the troubleshooter doesn't work, see the ["Troubleshoot Offline"](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues#troubleshoot-offline) section of the Update Agent troubleshooter guide
* Consult the [Update Agent Troubleshooter document](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues#prerequisite-checks) for any checks that failed in order to remediate issues

### **Error code like "Exception from HRESULT 0x..."**

* Follow the troubleshooting guide for ["Machine shows as Not Assessed and shows an HResult exception"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#hresult)

### **Machine shows as "not assessed"**

Information can take a few minutes to propagate through Log Analytics, but if machines still show "not assessed", then:

* Follow the troubleshooting guide for ["Scenario: Machines don't show up in the portal"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs)


### **Machines update without an update deployment**

* See the troubleshooting guide ["Scenario: Updates install without a deployment"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#updates-nodeployment)

### **Updating machines across different tenants**

* If you receive an error message saying "The current tenant is not authorized to access the linked subscription", please use [the workaround here](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#multi-tenant)

### **Updates aren't installing while "Never reboot" is selected"**

* Some updates can be dependent on other required updates. If a required update needs a reboot, and "Never reboot" is selected, the required update will not finish installing and any dependent updates will not be able to install until the next update deployment.
* Updates can also be skipped once the maintenance window is exceeded. See ["The scheduled update failed with a MaintenanceWindowExceeded error"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#mw-exceeded). 

### **Updates for other Microsoft products**

* By default, Windows Update provides updates only for Windows. To change this behavior, see [Enable updates for other Microsoft products](https://docs.microsoft.com/azure/automation/automation-configure-windows-update#enable-updates-for-other-microsoft-products)


## **Recommended Documents**

* [Troubleshoot issues using Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-management)
* [Troubleshoot issues onboarding Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/onboarding)
* [Understand the agent check results in Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues)
* [Update Management Overview](https://docs.microsoft.com/azure/automation/automation-update-management)
* [Update Management Tutorial](https://docs.microsoft.com/azure/automation/automation-tutorial-update-management)
* [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510)
