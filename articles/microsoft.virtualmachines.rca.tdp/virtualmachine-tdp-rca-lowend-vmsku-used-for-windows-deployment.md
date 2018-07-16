<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - lowend-vmsku-used-for-windows-deployment"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-lowend-vmsku-used-for-windows-deployment"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32411844"
	resourceTags="windows, linux"
	productPesIds="14749,15571"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the deployment is using a extra-small size for the deployment and Windows is not able to complete the initial provisioning successfully.
<!--/issueDescription-->

## Resolution
When creating and deploying the virtual machine, please specify a larger size in order for the deployment to succeed and for the virtual machine to complete initial startup.<br>

For information about other VM types and sizes in Azure for Windows, see [Windows VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes).<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to ensure less frequent deployment failures specific to this issue.
