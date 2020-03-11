
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
selfHelpType="resource"
supportTopicIds="32612491"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
articleId="b4768e2c-86c7-41d7-9b22-d22709c8b1e5"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Move workspace to different subscription or resource group
You can move a Log Analytics workspace to a different resource group or subscription in the same region. When applicable, this also moves the associated Automation account (if exists) from one Azure subscription to another.<br>

**Important:** You can't move data from one Log Analytics workspace to another, or change the region that Log Analytics data is stored in.

## **Recommended Steps**

* To move a workspace to different subscription or resource group, you must unlink the Automation account in the workspace first. Unlinking an Automation account requires the removal of these solutions if they are installed in the workspace: *Update Management*, *Change Tracking*, or *Start/Stop VMs during off-hours*<br>
* After solutions are removed, unlink Automation account by selecting *Linked workspaces* on the left pane in Automation account resource and click *Unlink workspace* on the ribbon<br>
    * **Important:** The removed solutions should be installed and Automation account link to the workspace should to be defined after the workspace move.<br>

**Through the Azure Portal**<br>

* Click *change Resource group or Subscription name* in *essential* pen in your workspace. A new page opens with a list of resources - select the resources to move, complete the information then click *OK*. If you encounter an error, you can use the PowerShell cmdlet that produces a more verbose error message.

**Through the PowerShell cmdlet**<br>

* [Move-AzureRmResource](https://docs.microsoft.com/powershell/module/AzureRM.Resources/Move-AzureRmResource)<br>

## **Recommended Documents**

* [Move resources to new resource group or subscription](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources) 
