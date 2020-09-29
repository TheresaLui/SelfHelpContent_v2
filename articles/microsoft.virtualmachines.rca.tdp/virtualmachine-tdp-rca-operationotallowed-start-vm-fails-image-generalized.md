<properties
	pageTitle="Start  Failure RCA"
	description="RCA - operationotallowed start vm fails image is generalized"
	infoBubbleText="Found recent start failure. See details on the right."
	service="microsoft.compute"
	resource="virtualmachines"
	authors="scottAzure"
	ms.author="rashan, scotro"
	displayOrder=""
	articleId="DeploymentFailure_RCA-operationotallowed-start-vm-fails-image-generalized"
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
We have detected that the **<!--$OperationType-->operationType<!--/$OperationType-->** operation for virtual machine **<!--$vmname-->Virtual machine<!--/$vmname-->** initiated at **<!--$StartTime-->StartTime<!--/$StartTime--> (UTC)** encountered an issue due to the image being generalized.
<!--/issueDescription-->

## **Recommended Steps**

A generalized VM is a virtual machine with personal account information removed so that its image can be used for creating other VMs. There is no way to return the VM that generated this error back to its original state as a functioning virtual machine, however the following options may be helpful:

- Replace the VM by recreating it from the VHD used to create the original VM
- Create a new VM from the image used to create the original VM
- Create a new VM with a VHD that contains the user accounts, applications, and other state data from your original VM. Attach the VHD as the OS disk.<br>

We apologize for any inconvenience this may have caused you. We are continuously working on improving the platform to ensure less frequent deployment failures specific to this issue.<br>

## **Recommended Documents**

To learn more about generalized and specialized VMs for **Windows**:<br>

* [Learn how to prepare a Windows VHD to upload to Azure](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image)<br>
* [Learn how to use a specialized image](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized)<br>
* [Learn how to use a generalized image](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-generalized-managed)<br>
* [Learn how to generalize your Windows VM and create an image from it.](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource)<br>

To learn more about generalized and specialized VMs for **Linux**:<br>

* [Learn how to use a generalized image](https://docs.microsoft.com/azure/virtual-machines/linux/capture-image)<br>
* [Learn how to use a specialized image](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-generic)<br>
