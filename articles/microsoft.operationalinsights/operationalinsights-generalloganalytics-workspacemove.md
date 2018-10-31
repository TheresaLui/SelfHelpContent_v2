
<properties
pageTitle="Move workspace to different subscription or resource group"
description="Move workspace to different subscription or resource group"
service="microsoft.operationalinsights"
resource="workspaces"
symptomID=""
infoBubbleText=""
authors="yossiy"
displayorder="1"
selfHelpType="resource"
supportTopicIds="32612491"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
/>

# Move workspace to different subscription or resource group
You can move a Log Analytics workspace to a different resource group or subscription, in the same region. When applicable, this also moves the associated Automation account (if exists) from one Azure subscription to another.<br>

**Important:** You can't move data from one Log Analytics workspace to another, or change the region that Log Analytics data is stored in.

## **Recommended steps**<br>
* To move a workspace to different subscription or resource group, you must First you must unlink the Automation account in the workspace. Unlinking an Automation requires the removal these solutions if they are installed in the workspace: *Update Management*, *Change Tracking*, or *Start/Stop VMs during off-hours* are removed<br>
* After these solutions are removed, unlink Automation account by selecting *Linked workspaces* on the left pane in Automation account resource and click *Unlick workspace* on the ribbon<br>
    * **Important:** Removed solutions need to be re-installed in the workspace and Automation link to the workspace needs to be re-stated after the move<br>

**Through the Azure Portal**<br>
* Click *change* Resource group or Subscription name in *essential* pen in your workspace. A new page opens with a list of resources, select the resources to move, fill the information then click *OK*.If you encounter an error, you can use the PowerShell cmdlet, which can produce a more verbose error message<br>

**Through the PowerShell cmdlet**<br>
* [Move-AzureRmResource](https://docs.microsoft.com/powershell/module/AzureRM.Resources/Move-AzureRmResource)<br>

## **Recommended documents**<br>
* [Move resources to new resource group or subscription](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources) 