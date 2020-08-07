<properties
	pageTitle="Allocation Failure RCA SkuRegRec"
	description="AllocationFailed create standalone VM SkuRegRec"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="AllocationFailure_RCA-create-standalone-SkuRegRec"
	diagnosticScenario="AllocationFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>
# We ran diagnostics on your resource and found an issue

The Region this VM is associated with did not have enough capacity for the requested VM size at the time of deployment to support its allocation.<br>

>We are currently experiencing high demand for specific regions across the globe. For further information, please review our [commitment to customers and Microsoft Cloud Services continuity](https://aka.ms/CloudCovidResponseFAQ).<br>

<!--issueDescription-->
Based on the analysis of deployment failure: **<!--$CorrelationId-->CorrelationId<!--/$CorrelationId-->**, we saw that deployment failed for the resource **<!--$vmname-->myVM<!--/$vmname-->** in region: **<!--$Region-->Region<!--/$Region-->** for size: **<!--$VMSize-->VMSize<!--/$VMSize-->** due to an allocation failure.<br>

**<!--$SkuRegRec-->No information provided<!--/$SkuRegRec-->**<br>
<!--/issueDescription-->

## **Recommended Steps**

Consider the above alternate VM sizes and/or Regions for your deployment. These recommendations are generated based on the current capacity conditions. If you see the originally requested region and size in the recommendations, please try creating the VM again as the issue might have been temporary and there could be sufficient resources for allocation currently.<br>

| To determine sizes by ... | Do the following |
| --- | --- |
| Azure portal | Select the VM in the Azure portal. Under **Settings**, choose **Size**. On the **Size** blade, you can view available sizes and use filter options. |
| PowerShell | Use the [Get-AzComputeResourceSku](https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku) command and filter for a region:<br>`Get-AzComputeResourceSku` &vert; `where {$_.Locations.Contains("<<insert-region>>")}` |
 Azure CLI | Use the [az vm list-skus](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-skus) command with the `--location` parameter to filter for a region and the `--size` parameter to match the size name:<br>`az vm list-skus --location <<insert-region>> --size <<insert-size>> --output table`|
| REST API| Use the [Resource SKUs - List](https://docs.microsoft.com/rest/api/compute/resourceskus/list) operation.|<br>

You can also peruse [Products available by region](https://azure.microsoft.com/global-infrastructure/services/?products=virtual-machines) to see which products are available in all the regions.
