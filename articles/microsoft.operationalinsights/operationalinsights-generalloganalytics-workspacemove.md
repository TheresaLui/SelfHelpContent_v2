
<properties
pageTitle="Move workspace to different subscription or resource group"
description="Move workspace to different subscription or resource group"
service="microsoft.operationalinsights"
resource="workspaces"
symptomID=""
infoBubbleText=""
authors="yossiy"
ms.author="yossiy"
displayorder="8"
selfHelpType="generic"
supportTopicIds="32612491"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax, Mooncake, usnat, ussec"
articleId="b4768e2c-86c7-41d7-9b22-d22709c8b1e5"
ownershipId="AzureMonitoring_LogAnalytics"
/>

# Move workspace to different subscription or resource group
You can move a Log Analytics workspace to a different resource group or subscription in the same region. When applicable, this also moves the associated Automation account (if exists) from one Azure subscription to another.<br>

[Workspace move considerations](https://docs.microsoft.com/azure/azure-monitor/platform/move-workspace#workspace-move-considerations):
* Review [Move a Log Analytics workspace to different subscription or resource group article](https://docs.microsoft.com/azure/azure-monitor/platform/move-workspace)
* Subscriptions (source and destination) have to be within the same Azure Active Directory tenant and region
* Managed solutions that are installed in the workspace will be moved with the Log Analytics workspace
* Connected agents will remain connected and keep sending data to the workspace after the move
* Linked resources must be [removed](https://docs.microsoft.com/azure/azure-monitor/platform/move-workspace#delete-in-azure-portal) from the workspace along with solutions relying on automation account:<br>
  * Update Management
  * Change Tracking
  * Start/Stop VMs during off-hours<br>



## **Recommended Documents**

* [Move a Log Analytics workspace to different subscription or resource group article](https://docs.microsoft.com/azure/azure-monitor/platform/move-workspace)
* [Workspace move considerations](https://docs.microsoft.com/azure/azure-monitor/platform/move-workspace#workspace-move-considerations)
* [Move resources to new resource group or subscription](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources)
<br>
