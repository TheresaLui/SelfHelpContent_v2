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
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed because the deployment is using extra-small size for the deployment and Windows is unable to complete the initial provisioning successfully due to the resource limitations of an extra-small instance.
<!--/issueDescription-->

## Resolution
When creating and deploying the virtual machine, please specify a larger size in order for the deployment to succeed and for the virtual machine to complete initial startup.<br>

For information about other VM types and sizes in Azure for Windows, see [Windows VM sizes](https://docs.microsoft.com/azure/virtual-machines/windows/sizes).<br>

We apologize for any inconvenience this may have caused you.<br>
