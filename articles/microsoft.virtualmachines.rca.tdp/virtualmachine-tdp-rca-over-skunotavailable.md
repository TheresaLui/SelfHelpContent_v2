<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - rca-skunotavailable"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.authors="scotro"
	displayOrder=""
	articleId="DeploymentFailure_RCA-skunotavailable"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32411844"
	resourceTags="windows, linux"
	productPesIds="14749,15571"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because of a restriction on the SKU that you are trying to deploy.<br>
<!--/issueDescription-->

These restrictions are put in place due to numerous business and technical constraints some of which include capacity limitations. We apologize for any inconvenience this may have caused you. We are continuously working on expanding coverage for as many sizes in as many locations as possible.<br> 

To help you with this current issue, we suggest a couple of solutions:

1. **Consider Alternate Sizes or Locations:**<br>
 We encourage you to consider an alternate location or VM Size that meets your business needs. Azure provides several ways to query which SKUs are available. See [Resolve errors for SKU not available](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-sku-not-available-errors) to understand how to use [PowerShell](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-sku-not-available-errors#solution-1---powershell) and [Azure CLI](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-sku-not-available-errors#solution-2---azure-cli) to determine which SKUs are available in a specific region.<br>

2.	**Request Exemption:**<br> 
 If you are unable to find suitable alternate locations or VM sizes and would like to submit a request for an SKU to be enabled, follow the support request process described in [Region or SKU unavailable](https://docs.microsoft.com/azure/azure-supportability/sku-series-unavailable).  This action will streamline your request and assist in getting a faster turnaround time.<br>

## Related documents

* [Resolve errors for SKU not available](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-sku-not-available-errors)
* [Region or SKU unavailable](https://docs.microsoft.com/azure/azure-supportability/sku-series-unavailable)


