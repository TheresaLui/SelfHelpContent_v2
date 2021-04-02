<properties
	pageTitle="Deployment Failure RCA"
	description="Root cause analysis for 'SKU not available' when deploying a new virtual machine."
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="mibufo"
	ms.author="v-mibufo"
	displayOrder=""
	articleId="virtualmachine-tdp-gt-rca-skunotavailable-newvm"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32411844"
	resourceTags="windows, linux"
	productPesIds="14749,15571"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment of VM size **<!--$VMSize-->VM Size<!--/$VMSize-->** in region **<!--$Region-->Region<!--/$Region-->** failed because of a **<!--$RestrictionType-->Restriction Type<!--/$RestrictionType-->** restriction on the SKU that you are trying to deploy.
<!--/issueDescription-->

These restrictions are put in place due to numerous business and technical constraints, some of which include capacity limitations. We apologize for any inconvenience this may have caused you. We are continuously working on expanding coverage for as many sizes in as many locations as possible.

## **Recommended Steps**

1. **Consider Alternate Sizes or Locations**

	To see the list of sizes that are available for deployment for subscription **<!--$SubscriptionID-->SubscriptionID<!--/$SubscriptionID-->**, you can use the Azure CLI command [az vm list-skus](https://docs.microsoft.com/cli/azure/vm#az-vm-list-skus) to check for the VM sizes available in a region, and any deployment restrictions on the VM size.

2. **Request Exemption**

	If the size you desire is not listed, or is marked **NotAvailableForSubscription**, please follow the steps in [Troubleshooting region or SKU subscription issues](https://docs.microsoft.com/azure/azure-supportability/sku-series-unavailable) to submit a streamlined request for accessing the SKU size. This action will assist in getting a faster turnaround time.<br>

## **Recommended Documents**

To determine sizes available for your subscription, use one of the following methods:

- **PowerShell:** See the [Get-AzComputeResourceSku](https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku) command
- **Azure CLI:** See the [az vm list-skus](https://docs.microsoft.com/cli/azure/vm#az-vm-list-skus) command
- **REST API:** See the [Resource SKUs - List](https://docs.microsoft.com/rest/api/compute/resourceskus/list) operation
