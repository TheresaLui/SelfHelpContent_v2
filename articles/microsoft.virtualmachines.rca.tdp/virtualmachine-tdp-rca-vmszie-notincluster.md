<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - VM size not in cluster"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_RCA-VMSizeValidation_NotInCluster_OperationFailure"
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

Please choose a different VM size. You might need to use a different image and size (SKU) depending on your region.

To determine available SKUs using PowerShell, Azure CLI, or the Azure Portal, see [Resolve errors for SKU not available](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-sku-not-available-errors). To resove SKU issues for a region according to a subscription, see [Region or SKU unavailable](https://docs.microsoft.com/azure/azure-supportability/sku-series-unavailable).

