<properties
	pageTitle="Deployment Failure RCA"
	description="RCA - osprofile-not-allowed-on-existing-specialized-disk"
	infoBubbleText="Found recent deployment failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	displayOrder=""
	articleId="DeploymentFailure_rca-virtualmachine-tdp-rca-osprofile-not-allowed-on-existing-specialized-disk"
	diagnosticScenario="DeploymentFailure"
	selfHelpType="rca"
	supportTopicIds="32411844"
	resourceTags="windows, linux"
	productPesIds="14749,15571"
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed as OSProfile was defined as part of the deployment but the VM has been classified as specialized.
<!--/issueDescription-->

Possible solutions:<br>

* Remove *[osProfile](https://docs.microsoft.com/azure/templates/microsoft.compute/virtualmachines#OSProfile)* from your deployment as this is only required if the VHD has been generalized for either [Linux](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-generic) or [Windows](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource).<br>
* Verify that your deployment is using *"createOption": "fromImage"* and not *"createOption": "Attach"* if you are provisioning a generalized image.
