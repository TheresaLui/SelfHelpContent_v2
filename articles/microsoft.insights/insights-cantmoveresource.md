<properties 
    pageTitle="I can't move an Application Insights resource"
    description="I can't move an Application Insights resource"
    service="microsoft.insights"
    resource="components"
    authors="mcosner"
    displayOrder="13"
    selfHelpType="resource"
    cloudEnvironments="public"
 />
# I can't move an Application Insights resource
## **Recommended steps**
To ensure that you are able to successfully move a resource to a different resource group and/or subscription:

1. Moving a resource to a different location is not supported, regardless of the location of the destination resource group or resources contained in that resource group.  
2. Ensure that in cases where you wish to move an Application Insights resource along with all associated webtests and alerts, that you select **only** the Application Insights resource.  All alerts and webtests will be automatically moved along with the Application Insights resource they are associated with.  If you accidentally selected an alert rule and an Application Insights resource in the same move operation, you might see an error message that contains the following text:

```
...there is alert rule not belong to any components in the resoruces list:/subscriptions/<yoursub>...
```
3. Review the [checklist before moving resources](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources#checklist-before-moving-resources) which describes some other general limitations on moving resources and examples from the Portal, Azure CLI, and Azure PowerShell.

Note that it is required to contact support to move your resources to a new Azure account (and Azure Active Directory tenant).

## **Recommended documents**
[Understand how to move resources to a new resource group or subscription](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)
