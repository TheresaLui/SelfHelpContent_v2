<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - rca-over-constrained-allocation-paas"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_RCA-over_constrained_allocation_paas"
	diagnosticScenario="DeploymentFailure,"
	selfHelpType="rca"
	supportTopicIds="32565644,32565474,32565475,32565476,32565478,32565479,32565480"
	resourceTags=""
	productPesIds="13185"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for cloud service **<!--$csname-->cloud service<!--/$csname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to an [allocation failure](https://docs.microsoft.com/azure/cloud-services/cloud-services-allocation-failures#solutions).
<!--/issueDescription-->
This issue is commonly caused by one of the following:<br>

* The virtual machine size requested in the deployment is not supported in the selected region: check if the [virtual machine sizes](https://azure.microsoft.com/regions/services) you selected are supported in the targeted region.<br>
* If you are updating an existing deployment, the cluster where your cloud service is hosted may have ran out of available capacity to complete your request: Try starting a new deployment for a new cloud service or select a smaller VM size.<br> 

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to ensure less frequent deployment failures specific to this issue.<br>
