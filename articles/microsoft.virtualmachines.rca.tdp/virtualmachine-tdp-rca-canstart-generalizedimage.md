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
	cloudEnvironments="public"
/>
# We ran diagnostics on your resource and found a start failure

<!--issueDescription-->
We have detected a start failure of your virtual machine with an error "Operation 'start' is not allowed as the VM is generalized". This occurs when an image capture operation was attempted incorrectly.
<!--/issueDescription-->

## **Recommended Steps**
Below are the scenarios that could lead to the VM start failure with this failure signature.
1. If a Sysprep has been run to generalize the VM before the capture option was selected and the VM is being started after that.
	* Once you have run sysprep on an VM it is considered generalized and it cannot be restarted. The process of generalizing a VM is not reversible.
	* Sysprep removes all your personal account information and the machine is prepared to be used as an image. For details about Sysprep, see [How to Use Sysprep: An Introduction.](http://technet.microsoft.com/library/bb457073.aspx)<br>
	* In order to restore the VM, please delete the VM and then navigate to the image "Images" section in portal, which was created as a result of the capture operation.
	* Create the VM from that image following the steps at [Create a VM from a managed  image.](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-generalized-managed?toc=%2fazure%2fvirtual-machines%2fwindows%2ftoc.json)


2. If a Sysprep has not been run prior to selecting the capture option, please delete the VM and recreate it from the same OS disk following detailed instructions in the below articles:
	* [Create a VM from a VHD using the Azure portal](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized-portal)
	* [Create a Windows VM from a specialized disk using PowerShell](https://docs.microsoft.com/azure/virtual-machines/windows/create-vm-specialized)

## **Recommended documents**
In order to avoid this issue in future, capture a VM image by following the instructions at [Create a managed image of a generalized VM in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource)
