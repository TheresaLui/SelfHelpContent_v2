

<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - max-quota-limit-exceeded"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-max-quota-limit-exceeded"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32411844"
	resourceTags="windows, linux"
	productPesIds="14749,15571"
	cloudEnvironments="public"
/>
# A recent request to deploy a virtual machine failed because it exceeded your available virtual CPU quota
<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to the virtual CPU quota being exceeded for the requested resource.
<!--/issueDescription-->

To deploy the desired VM, you must first increase your virtual CPU quota using the instructions below:<br>
* [How to view and increase your current quota](https://docs.microsoft.com/azure/azure-supportability/resource-manager-core-quotas-request)<br>

To learn more about how quotas are managed for Azure subscriptions, please refer to the following articles:<br>

* [Learn about the new Subscription Usage + Quotas view that displays your current limits](https://blogs.msdn.microsoft.com/skeeler/2017/01/subscription-usage-and-quotas-in-the-azure-portal/)  
* [Azure subscription and service limits, quotas, and constraints](https://docs.microsoft.com/azure/azure-subscription-service-limits)<br>
