<properties
	pageTitle="Allocation Failure RCA Allocation Success Recommender"
	description="AllocationFailed RCA Allocation Success Recommender"
	infoBubbleText="Allocation success recommendation found. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="summertgu"
	ms.author="tiag"
	displayOrder=""
	articleId="AllocationFailure_RCA-create-asr"
	diagnosticScenario="AllocationFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>
# We ran diagnostics on your requested parameters to provide guidance

The Allocation Success Recommender predicts the chance of success for your specified allocation based on the inputs specified. If your specified allocation is blocked or has a low chance of success, the Recommender provides alternate recommendations with high chance of success. Recommendations are ranked based on the likelihood of success.<br>

<!--issueDescription-->
Based on the analysis of your desired deployment allocation with the requested parameters: Subscription ID: **<!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId-->**, region: **<!--$Region-->Region<!--/$Region-->**, size: **<!--$VMSize-->VMSize<!--/$VMSize-->**, instances: **<!--$Instances-->Instances<!--/$Instances-->**.<br>

**<!--$SkuRegRec-->No alternate region or size recommendations<!--/$SkuRegRec-->**<br>

<!--/issueDescription-->

## **Recommended Steps**

Consider the alternate VM sizes and/or regions for your deployment. These recommendations are generated based on the current capacity conditions. If you see your originally requested region and size in the recommendations, try creating the VM again, because the issue might have been temporary and there may now be sufficient resources.<br>

| To determine sizes by ... | Do the following |
| --- | --- |
| Azure portal | Select the VM in the Azure portal. Under **Settings**, choose **Size**. On the **Size** blade, you can view available sizes and use filter options. |
| PowerShell | Use the [Get-AzComputeResourceSku](https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku) command and filter for a region:<br>`Get-AzComputeResourceSku` &vert; `where {$_.Locations.Contains("<<insert-region>>")}` |
 Azure CLI | Use the [az vm list-skus](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-skus) command with the `--location` parameter to filter for a region and the `--size` parameter to match the size name:<br>`az vm list-skus --location <<insert-region>> --size <<insert-size>> --output table`|
| REST API| Use the [Resource SKUs - List](https://docs.microsoft.com/rest/api/compute/resourceskus/list) operation.|<br>

Also review [Products available by region](https://azure.microsoft.com/global-infrastructure/services/?products=virtual-machines) to see which products are available in all the regions.
