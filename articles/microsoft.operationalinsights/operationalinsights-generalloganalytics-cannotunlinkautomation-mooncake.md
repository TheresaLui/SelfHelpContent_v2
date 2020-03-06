
<properties
    pageTitle="Cannot unlink Automation account"
    description="Cannot unlink Automation account"
    service="microsoft.operationalinsights"
    resource="workspaces"
    symptomID=""
    infoBubbleText=""
    authors="yossiy"
	ms.author="yossiy"
    displayorder="10"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="operationalinsights-generalloganalytics-cannotunlinkautomation-mooncake"
	ownershipId="ASEP_ContentService_Placeholder"
/>

# Cannot unlink Automation account

You need Contributor permission in the Resource Group level to perform this operation.

## **Recommended Steps**

To unlink an Automation account from a Log Analytics workspace you must first remove all solutions from the workspace that have dependencies on the Automation account, including:

* Update Management
* Change Tracking
* Start/Stop VMs during off-hours

After you remove these solutions from the workspace, you can continue with the unlinking following these steps:

* From Automation account, select *Linked workspace* on the left pane.
* Click *Unlink workspace* on the ribbon, then *OK*. 

## **Recommended Documents**

* [Azure Automation User Documentation](https://docs.azure.cn/automation/)
* [Forward job status and job streams from Automation to Log Analytics](https://docs.azure.cn/automation/automation-manage-send-joblogs-log-analytics)