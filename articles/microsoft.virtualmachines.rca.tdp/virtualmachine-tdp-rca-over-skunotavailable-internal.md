<properties
	pageTitle="Deployment failure - SKU not available (internal)"
	description="RCA - rca-skunotavailable"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_RCA-skunotavailable-internal"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags="windows, linux"
	productPesIds=""
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because of a restriction on the SKU that you were trying to deploy.
<!--/issueDescription-->

These restrictions are put in place due to numerous business and technical constraints, as well as capacity limitations. We apologize for any inconvenience this may have caused  you. We are continuously working on expanding coverage for as many sizes in as many locations as possible.

## Recommended steps

### Consider alternative sizes or locations

We encourage you to consider an alternate location or VM size that meets your business needs. You can use PowerShell or Azure CLI to query which SKUs are available. For more information see the following:

* [Resolve errors for SKU unavailable](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-sku-not-available-errors)
* [Region or SKU unavailable](https://docs.microsoft.com/azure/azure-supportability/sku-series-unavailable)<br>

### Request Exemption

If you are unable to find suitable alternate locations or VM sizes and are dependent on this specific combination, please let us know and we will see what options are available. If possible, will try to enable this VM Size and region for your subscription.

