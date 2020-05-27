<properties
	pageTitle="Deployment failure - SKU not available (internal)"
	description="Deployment failure - SKU not available (internal)"
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
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>
# Deployment Failure - SKU not available

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because of a restriction on the SKU that you were trying to deploy.
<!--/issueDescription-->

These restrictions are put in place due to numerous business and technical constraints, including capacity limitations. We apologize for any inconvenience this may have caused  you. We are continuously working on expanding coverage for as many sizes in as many locations as possible.

## **Recommended Steps**

### Consider alternative sizes or locations

We encourage you to consider an alternate location or VM size that meets your business needs. You can use PowerShell or Azure CLI to query which SKUs are available.

### Request exemption

If you are unable to find suitable alternate locations or VM sizes and are dependent on this specific combination, please let us know and we will see what options are available. If possible, we will try to enable this VM size and region for your subscription.

## **Recommended Documents**

* [Resolve errors for SKU unavailable](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-sku-not-available-errors)
* [Region or SKU unavailable](https://docs.microsoft.com/azure/azure-supportability/sku-series-unavailable)<br>
