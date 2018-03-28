<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - rca-skunotavailable"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because of a restriction on the SKU that you are trying to deploy.
* There are currently not enough cores of the VM Size Family you requested in this region.
<!--/issueDescription-->

Over the past several months, we have experienced unprecedented growth in Azure demand in several Regions. While we have capacity to support this phenomenal expansion at a global level, sometimes a specific resource/region combination is not consistent across all active Azure Regions. In some Regions, the demand for a specific Azure resource may outstrip capacity, and while we are actively working to build out additional capacity, sometimes we have to make the difficult decision to restrict certain offer types in a few Regions. This temporary measure is to make sure the best possible experience for our customers as we work hard to alleviate a restriction situation. Also, if you have more subscriptions to whitelist, please share the subscription details and planned SKU size and numbers of VM’s / cores to deploy in the requested region.<br>

For additional information, please read the following documents:<br>

* Learn more about [resolving SKU Not Available errors](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-sku-not-available-errors).<br>
* Additional information on resolving [not having access to a region or a VM SKU](https://docs.microsoft.com/azure/azure-supportability/sku-series-unavailable).<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to ensure less frequent deployment failures specific to this issue.<br>
