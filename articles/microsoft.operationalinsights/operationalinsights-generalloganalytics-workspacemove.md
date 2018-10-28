
<properties
pageTitle="Move workspace to different subscription or resource group"
description="Move workspace to different subscription or resource group"
service="microsoft.operationalinsights"
resource="workspaces"
symptomID=""
infoBubbleText=""
authors="yossiy"
displayorder="100"
selfHelpType="resource"
supportTopicIds="32612491"
resourceTags=""
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
/>
# Move workspace to different subscription or resource group
You can move a Log Analytics workspace to a different resource group or subscription, in the same region. This also moves the associated Automation account (if exists) from one Azure subscription to another.
> Note: You can't move data from one Log Analytics workspace to another, or change the region that Log Analytics data is stored in.
## **Recommended steps**
* To move a workspace to different subscription or resource group, you must first unlink the Automation account in the workspace. Unlinking Automation requires that these solutions (if exist): *Update Management*, *Change Tracking*, or *Start/Stop VMs during off-hours* are removed
* After these solutions are removed, unlink Automation account by selecting *Linked workspaces* on the left pane in Automation account resource and click *Unlick workspace* on the ribbon
    >Removed solutions and Automation link to workspace needs to be re-stated after the move if needed
* Perform the *move* operation following these steps:
    * Azure Portal – Click *change* Resource group or Subscription name in *essential* pen in your workspace. A new page opens with a list of resources, select the resources to move, fill the information then click *OK*. When encountering an error, you can use the PowerShell cmdlet, which can produce a more verbose error message
    * PowerShell – Use [Move-AzureRmResource](https://docs.microsoft.com/powershell/module/AzureRM.Resources/Move-AzureRmResource) cmdlet



## **Recommended documents**
[Move resources to new resource group or subscription](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-move-resources) 