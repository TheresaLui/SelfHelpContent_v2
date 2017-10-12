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
#We detected a recent issue with your deployment attempt:
 
<!--issueDescription-->
We identified that your deployment failed for <!--$csname-->Cloud Service<!--/$csname-->:** at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. There are currently not enough cores of the VM Size Family you requested in the cluster hosting your Cloud Service. If the requested virtual machine size is supported in the region, then the cluster where your Cloud Service is hosted does not support the VM Size you are trying to deploy.
<!--/issueDescription-->

To learn more about self-mitigatation:<br>
* Products available by region, [follow these instructions](https://docs.microsoft.com/azure/cloud-services/cloud-services-allocation-failures#solutions)<br>

To learn more about sizes supported in each region:<br>
* Products available by region, [follow these instructions](https://azure.microsoft.com/regions/services)<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to ensure less frequent deployment failures specific to this issue.<br>