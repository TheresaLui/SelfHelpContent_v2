<properties
    pageTitle="Azure Automation - Change Tracking & Inventory isn't working"
    description="Azure Automation - Change Tracking & Inventory stopped working"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="zjalexander"
    ms.author="zachal"
    displayorder=""
    selfHelpType="generic"
    supportTopicIds="32599863,32599865,32599902,32599918"
    resourceTags=""
    productPesIds="15607"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="aad511bc-804b-4d75-8748-121f7ae222fe"
	ownershipId="Compute_Automation"
/>

# Azure Automation - Change Tracking and Inventory Isn't Working

## **Recommended Steps**

You can run the [offline version of the Agent Registration script](https://docs.microsoft.com/azure/automation/troubleshoot/update-agent-issues#troubleshoot-offline) to find more detailed troubleshooting on prerequisites for the Change Tracking and Inventory. Although this script performs some checks related to Update Management, most requirements are the same for Change Tracking and Inventory. 

### I am unable to onboard machines onto Change Tracking and Inventory

* Please review the [onboarding troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/onboarding)

### I am not seeing Change Tracking records for my Windows machine

* Please review the [Change Tracking troubleshooting guide](https://docs.microsoft.com/azure/automation/troubleshoot/change-tracking#records-not-showing-windows)
* Records are not collected immediately. See [Data Collection Details](https://docs.microsoft.com/azure/automation/change-tracking#change-tracking-data-collection-details)
* Windows client SKUs are not supported. Please see the [Supported Operating Systems list](https://docs.microsoft.com/azure/automation/change-tracking#supported-windows-operating-systems)

### I can't see Files tracked

* File Tracking must be enabled. See [Enable File Tracking](https://docs.microsoft.com/azure/automation/change-tracking-file-contents#enable-file-content-tracking).

### Some areas of Change Tracking are blank

* If you are using Azure Security Center and File Integrity Monitoring, please see [Configuring Change Tracking](https://docs.microsoft.com/azure/automation/change-tracking#file-integrity-monitoring-in-azure-security-center)


### I can't deploy Change Tracking into the region I want

* Only specific regions are supported. Review the [Workspace Mappings document](https://docs.microsoft.com/azure/automation/how-to/region-mappings).

## **Recommended Documents**

* [Change Tracking Overview](https://docs.microsoft.com/azure/automation/automation-change-tracking)<br>
* [Inventory Overview](https://docs.microsoft.com/azure/automation/automation-vm-inventory)<br>
* [Data to gather when opening a case for Azure Automation](https://docs.microsoft.com/azure/automation/troubleshoot/collect-data-microsoft-azure-automation-case)
