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
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>
# We cannot deploy the selected size of your resource

<!--issueDescription-->
We detected that the deployment for virtual machine **<!--$vmname-->myVM<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the VM size is not available in the region where you are trying to deploy it.<br>
<!--/issueDescription-->

The VM size selected for this VM cannot be created in the specified region. This limitation is due to business and technical constraints, some of which include capacity limitations. We apologize for any inconvenience this may have caused you. We are continuously working on expanding coverage for as many sizes in as many locations as possible.<br>

## **Recommended Steps**

Please try to redeploy your VM and refer to one of the available sizes in the region. You can determine available sizes as described in the following table.

| To determine sizes by ... | Do the following |
| --- | --- |
| Azure portal | Select the VM in the Azure portal. Under **Settings**, choose **Size**. On the **Size** blade, you can view available sizes and use filter options. |
| PowerShell | Use the [Get-AzComputeResourceSku](https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku) command and filter for a region:<br>`Get-AzComputeResourceSku` &vert; `where {$_.Locations.Contains("<<insert-region>>")}` |
 Azure CLI | Use the [az vm list-skus](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-skus) command with the `--location` parameter to filter for a region and the `--size` parameter to match the size name:<br>`az vm list-skus --location <<insert-region>> --size <<insert-size>> --output table`|
| REST API| Use the [Resource SKUs - List](https://docs.microsoft.com/rest/api/compute/resourceskus/list) operation.|<br>

You can also peruse [Products available by region](https://azure.microsoft.com/global-infrastructure/services/?products=virtual-machines) to see which products are available in all the regions.
