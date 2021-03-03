<properties
  pagetitle="Resolve Update Management issues with Azure Automation - Scanning for Updates&#xD;"
  description="Resolve Update Management issues with Azure Automation"
  service="microsoft.automation"
  resource="automationaccounts"
  ms.author="zachal,riyadav"
  selfhelptype="Generic"
  supporttopicids="32615228"
  resourcetags=""
  productpesids="15607,15725"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="754ca972-a640-407c-8f78-a0836b393a9d"
  ownershipid="Compute_Automation" />
# Resolve Update Management issues with Azure Automation - Scanning for Updates

This article can help with assessing available updates for machines enrolled in Update Management.

## **Recommended Steps**

For help with common configuration issues, review the Update Agent Troubleshooter for [Windows](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues) or [Linux](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues-linux).

### **Machine shows as "not assessed"**

* Information can take a few minutes to propagate through Log Analytics, but if machines still show "not assessed", follow the steps in the [Machines don't show up under Update Management guide](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs)
* If you see an error code like "Exception from HRESULT 0x...", follow the troubleshooting guide for [Machine shows as Not Assessed and shows an HResult exception](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#hresult)
* This error commonly indicates that an inaccessible WSUS server has been configured, or that Windows Update is not reachable on the network

### **KB2267602 is consistently shown as missing**

* KB2267602 is the [Windows Defender definition update](https://www.microsoft.com/wdsi/definitions). It is updated daily.

### **Updates show as missing even after deployment**

* Deploying updates to Linux by classification ("Critical and security updates") has important caveats, especially for CentOS. See limitations [here](https://docs.microsoft.com/azure/automation/update-management/view-update-assessments#linux).
* Check the [job logs](https://docs.microsoft.com/azure/automation/update-management/query-logs) of a deployment to see if updates were filtered out due to classification
* Updates are often superseded by other updates. See [Superseded update indicated as missing](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#scenario-superseded-update-indicated-as-missing-in-update-management).
* Some updates can be dependent on other required updates. If a required update needs a reboot, and **Never reboot** is selected, the required update will not finish installing. Any dependent updates will not be able to install until the next update deployment.
* Updates can be skipped when the maintenance window is exceeded. See ["The scheduled update failed with a MaintenanceWindowExceeded error"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#mw-exceeded). 

### **Machines update without an update deployment**

* This is due to Windows Update registry settings. Review [Scenario: Updates install without a deployment](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#updates-nodeployment).

### **Update Agent Readiness doesn't show as ready**

* Follow the steps in [Machines don't show up under Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs)

### **Update Management dashboard shows incorrect data**

* This can occur if you have exceeded your Log Analytics pricing tier. See the [Log Analytics pricing documentation](https://docs.microsoft.com/azure/azure-monitor/platform/manage-cost-storage#changing-pricing-tier) for assistance in diagnosing and resolving this problem. 

## **Recommended Documents**

* [Troubleshoot issues using Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/update-management)
* [Update Management - Get Started](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-manage-updates-for-vm)
* [Configure Windows Update Client Settings for Update Management](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-configure-wuagent)
