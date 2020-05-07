<properties
	pageTitle="Start Failure RCA"
	description="RCA - Cannot Start a VM with generalized image"
	infoBubbleText="The VM failed to start as its been generalized. Follow the mitigation steps on the right"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ram-kakani"
	displayOrder=""
	articleId="Startfailure_GeneralizedImage"
	diagnosticScenario="StartFailure"
	selfHelpType="rca"
	supportTopicIds="32411817"
	resourceTags="windows"
	productPesIds="14749"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="Compute_VirtualMachines_Content"
/>
# We ran diagnostics on your VM **<!--$vmname-->[vmname]**<!--/$vmname--> and found a start failure
<!--issueDescription-->
We have detected that your virtual machine **<!--$vmname-->[vmname]**<!--/$vmname--> failed to start with an error:
"Operation 'start' is not allowed as the VM is generalized". 

This error is caused by an incorrect attempt to run an image capture operation.

<!--/issueDescription-->

## **Recommended Steps**
Below are the scenarios that could lead to the VM start failure with this failure signature.<br>

**VM is being started after a Sysprep has been run to generalize before selecting the capture option.**<br>

Once you have run Sysprep on an VM it is considered generalized and it cannot be restarted. The process of generalizing a VM is not reversible. Sysprep prepares the VM to be used as an image by removing all your personal and account information from the virtual machine. For details about Sysprep, see [How to Use Sysprep: An Introduction.](http://technet.microsoft.com/library/bb457073.aspx)<br>

To restore the virtual machine, follow the steps below:<br>
* Delete the VM<br>
* Navigate to the image "Images" section in portal, to find the image that was created as a result of the prior capture operation.<br>
* Create the VM from that image following the steps at [Create a VM from a managed  image.](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-generalized-managed?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)<br>

**VM is being started after a capture option has been selected but a Sysprep has not been run**<br>

To restore the virtual machine, delete and recreate it from the same OS disk following instructions in the below articles.<br>
* [Create a VM from a VHD using the Azure portal](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized-portal)<br>
* [Create a Windows VM from a specialized disk using PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized)<br>

## **Recommended documents**
In order to avoid this issue in future, capture a VM image by following the instructions at [Create a managed image of a generalized VM in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource)
