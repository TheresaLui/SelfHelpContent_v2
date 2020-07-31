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
    cloudEnvironments="public, Fairfax, usnat, ussec, blackForest, mooncake"
    articleId="7784e652-9ef4-42a9-ac42-e13c9d604aba"
	ownershipId="Compute_Automation"
/>

# Resolve Update Management issues with Azure Automation - Update Deployment Didn't Install

This article will help for issues where machines are enrolled in Update Management, but an Update Deployment failed to install some or all updates.

## **Recommended Steps**
Update Management logs attempts to install updates. [Check the job output](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-deploy-updates#check-deployment-status) for errors. 

### **"Failed to Start"**

* This error is commonly caused by machines which are turned off at the time of the deployment. It can also be caused by network connectivity or a machine that has changed names. The ["Failed to Start"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#failed-to-start) troubleshooting guide gives specific steps on how to resolve this issue.

### **I know updates are available, but they don't show as needed on my machines**

* This often happens if machines are configured to get updates from WSUS/SCCM, but WSUS/SCCM have not approved the updates
  * The [Windows Update Agent troubleshooter](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues) can show if there is a WSUS server configured
  * If machines are configured for WSUS then [run the Client Diagnostics tool](https://docs.microsoft.com/windows-server/administration/windows-server-update-services/manage/wsus-tools) 

### **I can't find or install a specific update**

* Try running updates locally, without Update Management. If the update still fails, the issue is with the configuration of the update agent itself. See [Client Requirements](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-overview#client-requirements) for details. If the update succeeds, try [removing the machine from the solution](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-remove-features) and reinstalling. 
* Updates are often [superseded by other updates](https://docs.microsoft.com/windows/deployment/update/windows-update-troubleshooting#the-update-is-not-applicable-to-your-computer). The superseded update will no longer appear in Update Management, even if the [Inclusion feature](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-deploy-updates#schedule-an-update-deployment) is used to specify the KB number. 
* By default, Windows Update provides updates only for Windows. To change this behavior, see [Enable updates for other Microsoft products](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-configure-wuagent#enable-updates-for-other-microsoft-products)
* Some updates can be dependent on other required updates. If a required update needs a reboot, and "Never reboot" is selected, the required update will not finish installing and any dependent updates will not be able to install until the next update deployment.
* Updates can also be skipped once the maintenance window is exceeded. See ["The scheduled update failed with a MaintenanceWindowExceeded error"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#mw-exceeded). 
* Deploying updates to Linux by classification ("Critical and security updates") has important caveats, especially for CentOS. These [limitations are documented on the Update Management overview page](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-overview#linux-2).



### **"Exception from HRESULT 0x..."**

* Follow the troubleshooting guide for ["Machine shows as Not Assessed and shows an HResult exception"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#hresult)
  * This error commonly indicates an inaccessible WSUS server has been configured, or Windows Update is not reachable on the network.

  ### **"Sudo status check failed"**

  * Verify the [configuration of the nxautomationuser account in the sudoers file](https://docs.microsoft.com/azure/automation/troubleshoot/hybrid-runbook-worker#prompt-for-password). 


## **Recommended Documents**

* [Troubleshoot issues using Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-management)
* [Update Management Overview - Supported Clients, Permissions and Network Requirements](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-overview)
* [Configure Windows Update Client Settings for Update Management](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-configure-wuagent)
