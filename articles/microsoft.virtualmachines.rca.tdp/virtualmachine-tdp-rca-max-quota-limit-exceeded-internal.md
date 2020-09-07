<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - Maximum quota limit exceeded"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
    ms.author="scotro"
	displayOrder=""
	articleId="DeploymentFailure_rca-max-quota-limit-exceeded-internal"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds=""
	resourceTags="windows, linux"
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
/>
# Maximum quota limit exceeded

## We ran diagnostics on your resource and found an issue
<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because of exceeding the virtual CPU quota limits on the subscription.  
<!--/issueDescription-->

To deploy the desired VM, we need to increase the virtual CPU quota. If you agree to increasing the quota limits for the following subscription, please complete the following information and we will work to increase those limits.<br>

| Item | Needed data |
| --- | --- |
| Subscription ID | **<!--$SubscriptionID-->SubscriptionID<!--/$SubscriptionID-->**|
| Region | |
| VM Family | |
| Number of cores needed | |
 
To learn more about how quotas are managed for Azure subscriptions, see [Azure subscription and service limits, quotas, and constraints](https://docs.microsoft.com/azure/azure-subscription-service-limits).
