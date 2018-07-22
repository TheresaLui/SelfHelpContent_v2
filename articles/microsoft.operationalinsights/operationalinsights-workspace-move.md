
<properties
    pageTitle="Move workspace to a different subscription"
    description="Workspace/Move workspace to a different subscription"
    service="microsoft.operationalinsights"
    resource="workspaces"
	symptomID=""
	infoBubbleText=""
    authors="olegan"
    displayorder="1"
    selfHelpType="generic"
    supportTopicIds="32592254"
    resourceTags=""
    productPesIds="15725"
    cloudEnvironments=""
/>

# Moving workspace to a different subscription

## **Recommended steps**
You can use Azure Portal to move a Log Analytics workspace to a different resource group or subscription, in the same region. This also moves the associated Automation account (if exists) from one Azure subscription to another.

When encountering an error, use the [Move-AzureRmResource](https://docs.microsoft.com/powershell/module/AzureRM.Resources/Move-AzureRmResource) cmdlet which can produce a more verbose error message.

Note: You can not move data from one Log Analytics workspace to another, or change the region that Log Analytics data is stored in.

## **Recommended documents**
[Move-AzureRmResource](https://docs.microsoft.com/powershell/module/AzureRM.Resources/Move-AzureRmResource) 