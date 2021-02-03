<properties
	pageTitle="I need guidance preparing an image"
	description="I need guidance preparing an image"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	ms.author="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32628272"
	resourceTags=""
	productPesIds="14749"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="a316fb37-cb8c-4b94-bdb1-276b2d90a555"
	ownershipId="Compute_VirtualMachines_Content"
/>

# I need guidance preparing an image

4 out of 5 customers resolved their issue with the guides listed below.<br>

## **Recommended Steps**

1. Review the following documents:<br>

	- [Microsoft server software support for Microsoft Azure virtual machines](https://support.microsoft.com/help/2721672/microsoft-server-software-support-for-microsoft-azure-virtual-machines)<br>
	- [Support for 32-bit operating systems in Azure](https://support.microsoft.com/help/4021388/support-for-32-bit-operating-systems-in-azure-virtual-machines)<br>
	- [Upload a generalized VHD and use it to create new VMs in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/upload-generalized-managed)
	- [Prepare a Windows VHD or VHDX to upload to Azure](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image)

2. Verify that your image was properly prepared:<br>

	- [Convert the virtual disk to VHD and fixed size disk](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image#convert-the-virtual-disk-to-vhd-and-fixed-size-disk)<br>
	- [Set Windows configurations for Azure](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image#set-windows-configurations-for-azure)<br>
	- [Check the Windows services](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image#check-the-windows-services)<br>
	- [Update Remote Desktop registry settings](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image#update-remote-desktop-registry-settings)<br>
	- [Configure Windows Firewall Rules](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image#configure-windows-firewall-rules)<br>
	- [Verify VM is healthy, secure, and accessible with RDP](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image#verify-vm-is-healthy-secure-and-accessible-with-rdp)<br>
	- [Complete recommended configurations](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image#complete-recommended-configurations)<br>

3. [Upload the VHD to your storage account](https://docs.microsoft.com/azure/virtual-machines/windows/upload-generalized-managed#upload-the-vhd-to-your-storage-account)<br>
4. [Create a managed image from the uploaded VHD](https://docs.microsoft.com/azure/virtual-machines/windows/upload-generalized-managed#create-a-managed-image-from-the-uploaded-vhd)<br>
5. [Create the VM](https://docs.microsoft.com/azure/virtual-machines/windows/upload-generalized-managed)
6. [Open any ports or endpoints](https://docs.microsoft.com/azure/virtual-machines/windows/nsg-quickstart-portal)

**Note:** If capturing an image already in Azure, follow the instructions for [capturing a VM to image in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource).<br>

**Who do I contact for technical support with a solution purchased in the Azure Marketplace?**<br>

Please contact your Azure Marketplace publisher for all technical product support. You can find publisher contact information and/or a link to the support website on their solution details page on Azure Marketplace.<br>

## **Recommended Documents**

* [Deploy or create Windows client operating systems in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/client-images)
* [Prepare a Windows VHD or VHDX to upload to Azure](https://docs.microsoft.com/azure/virtual-machines/windows/prepare-for-upload-vhd-image)<br>
* [Use Windows client in Azure for dev/test scenarios](https://docs.microsoft.com/azure/virtual-machines/windows/client-images)
* [Create a managed image of a generalized VM in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource)<br>
* [Create or clone a managed image of a generalized VM in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/capture-image-resource)<br>
* [Upload a generalized VHD and use it to create new VMs in Azure](https://docs.microsoft.com/azure/virtual-machines/windows/upload-generalized-managed)<br>
* [Troubleshoot deployment issues when creating a new virtual machine in Azure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-deploy-vm-windows)
