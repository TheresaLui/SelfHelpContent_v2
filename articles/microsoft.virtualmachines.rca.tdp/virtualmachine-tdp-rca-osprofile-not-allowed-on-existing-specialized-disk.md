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
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
We have detected that the deployment for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** failed due to  [OSProfile](https://docs.microsoft.com/azure/templates/microsoft.compute/virtualmachines#OSProfile) was present as part of the deployment action. OSProfile cannot be defined when the image is being deployed as specialized.
<!--/issueDescription-->

## Possible solutions:

* If the image being deployed has been specialized, or captured from an image, for either [Linux](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-generic) or [Windows](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource) operating systems, ***[osProfile](https://docs.microsoft.com/azure/templates/microsoft.compute/virtualmachines#OSProfile)***  must be removed from the deployment action. For additional info about *osProfile*, refer to this [document](https://docs.microsoft.com/azure/templates/microsoft.compute/virtualmachines#OSProfile).<br>

		"osProfile": {
			 "computerNamePrefix": "myvmss",
			 "adminUsername": "azureuser",
			 "adminPassword": "P@ssw0rd!"
		 }

* Verify that your deployment is consuming the correct value for *createoption* when using a generalized image *("createOption": "fromImage")* versus specialized image *("createOption": "Attach")*. For more information to understand the correct parameter, refer to this [document](https://docs.microsoft.com/powershell/module/azurerm.compute/set-azurermvmosdisk).<br>

		Powershell:
			Set-AzureRmVMOSDisk -VM $VirtualMachine -Name "osDisk.vhd" -SourceImageUri "<path to vhd>" -VhdUri "<vhd uri>" -CreateOption fromImage -Linux

		Template:
			"osDisk": {
					"name": "[concat(parameters('vmName'), 'OSDisk')]",
					"caching": "ReadWrite",
					"createOption": "FromImage",
					"managedDisk": {
							storageAccountType": "[parameters('storageType')]"
							}
					}
