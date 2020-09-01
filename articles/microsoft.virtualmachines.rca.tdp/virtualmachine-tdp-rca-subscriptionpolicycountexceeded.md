<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - subscriptionpolicycountexceeded"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-subscriptionpolicycountexceeded"
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
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to the subscription policy count being exceeded for the requested resource.
<!--/issueDescription-->

To work around this issue, please increase your quota or service limit using the instructions below:<br>

To learn more about subscritions, please refer to the following articles:<br>
* [Azure subscription and service limits, quotas, and constraints](https://docs.microsoft.com/azure/azure-supportability/resource-manager-core-quotas-request)<br>
* [How to view your current quota increase your vCPU and Cores](https://docs.microsoft.com/azure/azure-subscription-service-limits)<br>
