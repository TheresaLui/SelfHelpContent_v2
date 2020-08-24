<properties
pageTitle="View Designer issue"
description="View Designer issue"
service="microsoft.operationalinsights"
resource="workspaces"
symptomID=""
infoBubbleText=""
authors="aul,shemers"
ms.author="aul,shemers"
displayorder=""
selfHelpType="generic"
supportTopicIds="32745417"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
articleId="operationalinsights-viewdesigner"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# Commonly asked questions about View Designer

_View Designer is in the process of being retired and will no longer be supported. We suggest users to use Azure Monitor Workbooks as the replacement_

### View Designer is missing from my Log Analytics Workspace

Users are required to have [contributor level permissions](https://docs.microsoft.com/azure/azure-monitor/platform/manage-access#manage-access-using-azure-permissions) for the Log Analytics Workspace, otherwise the View Designer option will not be displayed in the menu.

### How do I share my View Designer visualizations?

Users that you wish to share the content with must also have contributor level permissions to the Log Analytics Workspace you are using. Users can access these views using the Workspace Summary for that Log Analytics Workspace.

For users concerned about Role-Based Access Control (RBAC), then consider using Azure Monitor Workbooks, where sharing generates a custom link, and does not require contributor level permissions for viewing shared Workbooks.

### How do I add other types of charts or visualizations?

View Designer only offers a set number and type of visualizations, to try out other visualizations, use Azure Monitor Workbooks.

### How do I change the size of my tiles?

View Designer restricts users to fixed tile sizes, consider using Azure Monitor Workbooks if this is limiting functionality of your visualizations.

### How do I load templates into View Designer?

If you have an existing file with extension .omsview, then you can use the `Import` button from the top toolbar to load a template.

Azure Monitor Workbooks offers templates pre-loaded into the gallery for users to open with a single click, or users can also upload their custom template JSON via the `</> Advanced Editor`

## **Recommended Documents**
 
[View Designer Documentation](https://docs.microsoft.com/azure/azure-monitor/platform/view-designer)
 
[View Designer to Workbooks](https://docs.microsoft.com/azure/azure-monitor/platform/view-designer-conversion-overview)
 
[Workbooks GitHub Repo](https://github.com/microsoft/Application-Insights-Workbooks/tree/master/Workbooks)
 