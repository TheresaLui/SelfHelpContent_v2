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
    cloudEnvironments="public, Fairfax"
    articleId="754ca972-a640-407c-8f78-a0836b393a9d"
	ownershipId="Compute_Automation"
/>

# Resolve Update Management issues with Azure Automation - Scanning for and Deploying Updates

This article will help with assessing available updates and installing updates using the Azure Update Management solution.

## **Recommended Steps**

* Try running the Update Agent Troubleshooter for [Windows](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues) or [Linux](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues-linux)) which addresses many common issues

### **I know updates are available, but they don't show as needed on my machines**


* This often happens if machines are configured to get updates from WSUS/SCCM, but WSUS/SCCM have not approved the updates
* [Check if machines are configured for WSUS/SCCM](https://support.microsoft.com/help/328010/how-to-configure-automatic-updates-by-using-group-policy-or-registry-s)
* If machines are configured for WSUS then [run the Client Diagnostics tool](https://docs.microsoft.com/windows-server/administration/windows-server-update-services/manage/wsus-tools) 


### **I can't find or install a specific update**

* Updates are often [superseded by other updates](https://docs.microsoft.com/windows/deployment/update/windows-update-troubleshooting#the-update-is-not-applicable-to-your-computer). The superseded update will no longer appear in Update Management, even if the [Inclusion feature](https://docs.microsoft.com/azure/automation/automation-tutorial-update-management#schedule-an-update-deployment) is used to specify the KB number. 


### **Machine shows as "not assessed"**

* Information can take a few minutes to propagate through Log Analytics, but if machines still show "not assessed", follow the steps in ["Machines don't show up under Update Management" ](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs)
* If you see an error code like "Exception from HRESULT 0x...", follow the troubleshooting guide for ["Machine shows as Not Assessed and shows an HResult exception"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#hresult)


### **Update run returns status "Failed"**

* Follow the troubleshooting guide for ["Update run returns status 'Failed'"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#scenario-update-run-returns-status-failed)


### **KB2267602 is consistently shown as missing**

* KB2267602 is the [Windows Defender definition update](https://www.microsoft.com/wdsi/definitions). It is updated daily.

### **Installing updates by classification on Linux**

* Deploying updates to Linux by classification ("Critical and security updates") has important caveats, especially for CentOS. These [limitations are documented on the Update Management overview page](https://docs.microsoft.com/azure/automation/automation-update-management#linux-2)

### **Machines update without an update deployment**

* See the troubleshooting guide ["Scenario: Updates install without a deployment"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#updates-nodeployment)

### **Updating machines across different tenants**

* If you receive an error message saying "The current tenant is not authorized to access the linked subscription", please use [the workaround here](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#multi-tenant)

### **Update Agent Readiness doesn't show "ready"**

* Follow the steps in ["Machines don't show up under Update Management" ](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs)

### **Update Management dashboard shows incorrect data**

* This can occur if you have exceeded your Log Analytics pricing tier. See the [Log Analytics pricing documentation](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#changing-pricing-tier) for assistance in diagnosing and resolving this problem.. 


## **Recommended Documents**

* [Troubleshoot issues using Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-management)
* [Troubleshoot issues onboarding Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/onboarding)
* [Understand the agent check results in Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues)
* [Update Management Overview](https://docs.microsoft.com/azure/automation/automation-update-management)
* [Update Management Tutorial](https://docs.microsoft.com/azure/automation/automation-tutorial-update-management)
* [Data to gather when opening a case for Azure Automation](https://support.microsoft.com/kb/3178510)
