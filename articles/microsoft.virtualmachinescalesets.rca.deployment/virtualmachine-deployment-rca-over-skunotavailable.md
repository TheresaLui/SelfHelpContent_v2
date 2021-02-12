<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - rca-skunotavailable"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachinescalesets"
	authors="summertgu"
	ms.author="tiag"
	displayOrder=""
	articleId="VMSS_DeploymentFailure_RCA-skunotavailable"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32641079,32641082,32641076,32641075,32641080,32641074,32641076,32641077,32641072,32641073"
	resourceTags=""
	productPesIds="16080"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachineScaleSets_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine scale set **<!--$vmssname-->Virtual machine scale set<!--/$vmssname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because of a restriction on the SKU that you are trying to deploy.<br>
<!--/issueDescription-->

These restrictions are put in place due to numerous business and technical constraints, some of which include capacity limitations. We apologize for any inconvenience this may have caused you. We are continuously working on expanding coverage for as many sizes in as many locations as possible.<br>

## **Recommended Steps**

1. **Consider Alternate Sizes or Locations**

	To see the list of sizes that are available for deployment for subscription **<!--$SubscriptionID-->SubscriptionID<!--/$SubscriptionID-->** , you can use the Azure CLI command [az vmss list-skus](https://docs.microsoft.com/cli/azure/vmss?view=azure-cli-latest#az-vmss-list-skus) to check for SKUs available for your VM scale set, including the minimum and maximum VM instances allowed for each SKU.

2. **Request Exemption**

	If the size you desire is not listed, or is marked **NotAvailableForSubscription**, please follow the steps in [Troubleshooting region or SKU subscription issues](https://docs.microsoft.com/azure/azure-supportability/sku-series-unavailable) to submit a streamlined request for accessing the SKU size. This action will assist in getting a faster turnaround time.<br>

## **Recommended Documents**

To determine sizes available for your subscription using <br>
* PowerShell: see [Get-AzComputeResourceSku](https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku) command
* Azure CLI: see [az vmss list-skus](https://docs.microsoft.com/cli/azure/vmss?view=azure-cli-latest#az-vmss-list-skus) command
* REST API: see [Virtual Machine Scale Sets - List Skus](https://docs.microsoft.com/rest/api/compute/virtualmachinescalesets/listskus) and [Resource SKUs - List](https://docs.microsoft.com/rest/api/compute/resourceskus/list) operations
