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
We identified that your deployment failed for <!--$csname-->Cloud Service<!--/$csname-->:** at **<!--$EndTime--> EndTime <!--/$EndTime--> (UTC)**. There are currently not enough cores of the VM Size Family you requested in the cluster hosting your Cloud Service. This is not a subscription quota issue and can be self-mitigated. To self-mitigate, please use a different VM Size or create a new Cloud Service with the desired VM Size. It is possible that the requested Virtual Machine size is not supported in the region.
<!--/issueDescription-->

Please use a different VM Size or create a new Cloud Service with the desired VM Size.<br>

To learn more about sizes supported in each region:<br>
* Products available by region, [follow these instructions](https://azure.microsoft.com/regions/services)<br>

To learn more about allocation failures with Cloud Services:
* [Learn more](https://docs.microsoft.com/en-us/azure/cloud-services/cloud-services-allocation-failures)<br>
* [Additional info for allocation failures](https://azure.microsoft.com/en-us/blog/allocation-failure-and-remediation)<br>
* [Additional info regarding sizes and cloud services](https://docs.microsoft.com/en-us/azure/cloud-services/cloud-services-sizes-specs)<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to ensure less frequent deployment failures specific to this issue.<br>