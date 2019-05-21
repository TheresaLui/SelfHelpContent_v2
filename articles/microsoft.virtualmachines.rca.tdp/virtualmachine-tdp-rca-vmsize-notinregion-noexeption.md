<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - VM size not in region"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_RCA-VMSizeValidation_NotInRegion"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>
# We cannot deploy the selected size of your resource

<!--issueDescription-->
We detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the VM size is not available in the region where you are trying to deploy it.<br>
<!--/issueDescription-->

The VM size selected for this VM cannot be created in the specified region. This limitation is due to business and technical constraints, some of which include capacity limitations. We apologize for any inconvenience this may have caused you. We are continuously working on expanding coverage for as many sizes in as many locations as possible.<br>

Please resize the VM to fix this issue. You can determine available sizes as described in the following table.

| To determine sizes by ... | Do the following |
| --- | --- |
| Azure Portal | Select the VM in the Azure Portal. Under **Settings**, choose **Size**. On the **Size** blade, you can view available sizes and use filter options. Select **Resize**. |
| PowerShell | Use the [Get-AzureRmVMSize](https://docs.microsoft.com/powershell/module/azurerm.compute/get-azurermvmsize) command. Use the `-Location` parameter to filter output for your region.|
| Azure CLI | Use the [az vm list-sizes](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-sizes) command. Use the `--location` parameter to filter output for your region.|
| REST | Use the [Resource SKUs - List](https://docs.microsoft.com/rest/api/compute/resourceskus/list) operation.|



