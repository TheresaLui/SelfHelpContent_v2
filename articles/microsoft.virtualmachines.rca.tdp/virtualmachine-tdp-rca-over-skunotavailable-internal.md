<properties
	pageTitle="Deployment failure - SKU not available (internal)"
	description="RCA - rca-skunotavailable"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_RCA-skunotavailable"
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

These restrictions are put in place due to numerous business and technical constraints, some of which include capacity limitations. We apologize for any inconvenience this may have caused  you. We are continuously working on expanding coverage for as many sizes in as many locatons as possible.

## Recommended steps

### Consider alterntive sizes or locations

We encourage you to consider an alternate location or VM size that meets your business needs. You can use PowerShell or Azure CLI to query which SKUs are available. For more information see the following:

* [Resolve errors for SKU unavailable](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-sku-not-available-errors)<br>
* [Region or SKU unavialable](https://docs.microsoft.com/azure/azure-supportability/sku-series-unavailable)<br>

### Mitigate with internal resources

You are encouraged to seeks solutions and contribute your observations in our internal wiki and knowledge bases:

- [CSS Support Wiki](https://www.csssupportwiki.com/index.php/curated:Azure/)
- [Azure Support Center](https://azuresupportcenter.msftcloudes.com)

