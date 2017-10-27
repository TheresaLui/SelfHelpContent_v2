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
# We detected a recent issue with your deployment attempt:

<!--issueDescription-->
We identified that your deployment failed for **<!--$csname-->Cloud Service<!--/$csname-->:** at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. 
<!--/issueDescription-->

This can happen due to one of the following reasons:<br>
* The Virtual Machine size requested is not supported in the region<br>
* The cluster where your Cloud Service is hosted does not have available capacity to complete your request. 

To learn more about sizes supported in each region, [review this document](https://azure.microsoft.com/regions/services)<br>

If the size is available in the region, self-mitgate by either deploying a new Cloud Service or changing the VM size for this Cloud Service.<br>

To learn more, [follow these instructions](https://docs.microsoft.com/azure/cloud-services/cloud-services-allocation-failures#solutions)<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to ensure less frequent deployment failures specific to this issue.<br>