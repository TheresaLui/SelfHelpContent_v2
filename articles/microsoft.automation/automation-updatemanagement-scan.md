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
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="754ca972-a640-407c-8f78-a0836b393a9d"
	ownershipId="Compute_Automation"
/>

# Resolve Update Management issues with Azure Automation - Scanning for Updates

This article will help with assessing available updates for machines enrolled in Update Management.

## **Recommended Steps**

The Update Agent Troubleshooter for [Windows](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues) or [Linux](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues-linux) can surface common configuration issues.

### **Machine shows as "not assessed"**

* Information can take a few minutes to propagate through Log Analytics, but if machines still show "not assessed", follow the steps in the ["Machines don't show up under Update Management"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs) guide
* If you see an error code like "Exception from HRESULT 0x...", follow the troubleshooting guide for ["Machine shows as Not Assessed and shows an HResult exception"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#hresult)
* This error commonly indicates an inaccessible WSUS server has been configured, or Windows Update is not reachable on the network

### **KB2267602 is consistently shown as missing**

* KB2267602 is the [Windows Defender definition update](https://www.microsoft.com/wdsi/definitions). It is updated daily.

### **Updates show as missing even after deployment**

* Deploying updates to Linux by classification ("Critical and security updates") has important caveats, especially for CentOS. These [limitations are documented on the Update Management overview page](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-view-update-assessments#linux).
* Check the [job logs](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-deploy-updates#view-results-of-a-completed-update-deployment) of a deployment to see if updates were filtered out due to classification
* Updates are often [superseded by other updates](https://docs.microsoft.com/windows/deployment/update/windows-update-troubleshooting#the-update-is-not-applicable-to-your-computer). The superseded update will no longer appear in Update Management, even if the [Inclusion feature](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-deploy-updates#schedule-an-update-deployment) is used to specify the KB number. 
* Some updates can be dependent on other required updates. If a required update needs a reboot, and "Never reboot" is selected, the required update will not finish installing and any dependent updates will not be able to install until the next update deployment.
* Updates can also be skipped once the maintenance window is exceeded. See ["The scheduled update failed with a MaintenanceWindowExceeded error"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#mw-exceeded). 

### **Machines update without an update deployment**

* This is due to Windows Update registry settings. See the troubleshooting guide ["Scenario: Updates install without a deployment"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#updates-nodeployment).

### **Update Agent Readiness doesn't show "ready"**

* Follow the steps in ["Machines don't show up under Update Management"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs)

### **Update Management dashboard shows incorrect data**

* This can occur if you have exceeded your Log Analytics pricing tier. See the [Log Analytics pricing documentation](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#changing-pricing-tier) for assistance in diagnosing and resolving this problem. 

## **Recommended Documents**

* [Troubleshoot issues using Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-management)
* [Update Management - Get Started](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-manage-updates-for-vm)
* [Configure Windows Update Client Settings for Update Management](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-configure-wuagent)
