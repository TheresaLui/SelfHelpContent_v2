<properties
	pageTitle="Virtual Machine Size Not Found RCA"
	description="Virtual Machine Size Not Found - Subscription"
	infoBubbleText="Found diagnostic result for the selected resource. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro,rashan"
	displayOrder=""
	articleId="SupportTopic_RCA-sizenotfound-default"
	diagnosticScenario="SizeNotFoundDefault"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>
# We ran diagnostics on your subscription

<!--issueDescription-->
We understand that you are unable to deploy your desired VM size in subscription **<!--$SubscriptionID-->SubscriptionID<!--/$SubscriptionID-->**.<br>
<!--/issueDescription-->

Deployment restrictions are put in place due to numerous business and technical constraints, some of which include capacity limitations. We apologize for any inconvenience this may have caused you. We are continuously working on expanding coverage for as many sizes in as many locations as possible.

## **Recommended Steps**

You can use the following steps to identify SKU restrictions and quota limitations for your subscription:<br>

- To see the list of sizes that are available for deployment for subscription **<!--$SubscriptionID-->SubscriptionID<!--/$SubscriptionID-->**, you can use the Azure CLI command [az vm list-skus](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-skus) to check for the VM sizes available by region and any deployment restrictions on the VM size. If the size you desire is not listed, or is marked **NotAvailableForSubscription**, please follow the steps in [Troubleshooting region or SKU subscription issues](https://docs.microsoft.com/azure/azure-supportability/sku-series-unavailable) to submit a streamlined request for accessing the SKU size. <br>
- To see the quota usage for subscription **<!--$SubscriptionID-->SubscriptionID<!--/$SubscriptionID-->**, you can use the Azure CLI command [az-vm-list-usage](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-usage). Quota limits are enforced at two tiers for each subscription, in each region. The first tier is the Total Regional vCPUs limit, and the second tier is the per VM Series vCPUs limit. If there is a quota limit that is preventing you from deploying your desired size, please follow the steps in [Quota increase requests](https://docs.microsoft.com/azure/azure-supportability/per-vm-quota-requests) to submit a streamlined request for increasing the limits.

## **Recommended Documents**

- To determine sizes available for your subscription, by region using PowerShell, use the [Get-AzComputeResourceSku](https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku) command, for Azure CLI see the [az vm list-skus](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-list-skus) command, for the REST API see the [Resource SKUs - List](https://docs.microsoft.com/rest/api/compute/resourceskus/list) operation.
