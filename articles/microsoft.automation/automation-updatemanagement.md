<properties
    pageTitle="Resolve Update Management issues with Azure Automation"
    description="Resolve Update Management issues with Azure Automation"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32642184,32599924,32642191,32633803,32633804,32743883,32745415"
    resourceTags=""
    productPesIds="15607,15725,14749,15571,15797,16454,16470, 15725"
    cloudEnvironments="public, Fairfax, usnat, ussec, blackForest, mooncake"
    articleId="6a3512a4-53ee-48c2-a748-f8cff1d4bb04"
	ownershipId="Compute_Automation"
/>

# Resolve Update Management issues with Azure Automation

This article will help with several kinds of issues relating to onboarding and using the Azure Update Management solution.
For general questions about Update Management scenarios, see [Update Management Overview](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-overview).

## **Recommended Steps**

The most common issues with Update Management are caused by:
* [Network issues](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-overview#ports) or [Windows Update registry keys](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-configure-wuagent), which can be detected by running the Update Agent Troubleshooter ([Windows](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues), [Linux](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues-linux))
* [Scope Configuration issues](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-scope-configuration), which can be detected by [querying Log Analytics](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#nologs)


### **Prerequisites for Update Management**
* The [Update Management Overview](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-overview) covers [supported clients](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-overview#clients), [required permissions](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-overview#permissions), and [network requirements ](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-overview#ports)
* Only certain regions are supported for linking Log Analytics and Automation Accounts, which is required for Update Management. See the ["Workspace Mappings"](https://docs.microsoft.com/azure/automation/how-to/region-mappings) document for the full list of supported regions.
* If your region is not listed as a supported region, you can [file a feedback request on our UserVoice](https://feedback.azure.com/forums/905242-update-management)


### **Remove machine from Update Management**

* To unenroll a machine from Update Management, Follow the instructions at ["Remove VMs from Update Management"](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-remove-vms)

### **Machines reboot unexpectedly**

* This behavior is caused by Windows Update registry keys. See ["Configure Reboot Settings"](https://docs.microsoft.com/azure/automation/update-management/update-mgmt-configure-wuagent#configure-reboot-settings)

### **Machines update without an update deployment**

* This behavior is caused by Windows Update registry keys which is configured to "Autodownload and install" by default for Azure VMs. See the troubleshooting guide ["Scenario: Updates install without a deployment"](https://docs.microsoft.com/azure/automation/troubleshoot/update-management#updates-nodeployment)


## **Recommended Documents**

* [Troubleshoot issues onboarding Update Management](https://docs.microsoft.com/azure/automation/troubleshoot/onboarding)
* [Automate onboarding Update Management](https://docs.microsoft.com/azure/cloud-adoption-framework/manage/azure-server-management/onboarding-automation)