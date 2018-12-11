<properties
	pageTitle="I am unable to deploy a captured or generalized image"
	description="I am unable to deploy a captured or generalized image"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="ScottAzure"
	authoralias="scotro"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32628259"
	resourceTags=""
	productPesIds="15571, 15797,16454"
	cloudEnvironments="public"
/>

# I am unable to deploy a captured or generalized image

4 out of 5 customers resolved their issue with the guides listed below.<br>
## **Recommended Steps**

Azure supports various Linux distributions (see Endorsed Distributions).

1. Following the instructions based on your Distro and prepare your image prior to upload.<br>

	- [Ubuntu](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-ubuntu)<br>
	- [CentOS-based](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-centos)<br>
	- [Red Hat-based](https://docs.microsoft.com/azure/virtual-machines/linux/redhat-create-upload-vhd)<br>
	- [Oracle](https://docs.microsoft.com/azure/virtual-machines/linux/oracle-create-upload-vhd)<br>
	- [Debian](https://docs.microsoft.com/azure/virtual-machines/linux/debian-create-upload-vhd)<br>
	- [SLES and openSUSE](https://docs.microsoft.com/azure/virtual-machines/linux/debian-create-upload-vhd)<br>
	- [Others: Non-Endorsed Distributions](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-generic)


2. [Upload the VM](https://docs.microsoft.com/azure/virtual-machines/linux/upload-vhd#option-1-upload-a-vhd)<br>

3. [Create the VM](https://docs.microsoft.com/azure/virtual-machines/linux/upload-vhd#create-the-vm)

4. [Open any ports or endpoints](https://docs.microsoft.com/azure/virtual-machines/linux/upload-vhd#next-steps)

## **Recommended Documents**

* [Create an image of a generalized VM in Azure](https://docs.microsoft.com/azure/virtual-machines/linux/capture-image)<br>
* [Upload a generalized VHD and use it to create new VMs in Azure](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-generic)<br>
* [Troubleshoot deployment issues when creating a new virtual machine in Azure](https://docs.microsoft.com/azure/virtual-machines/virtual-machines-linux-troubleshoot-deployment-new-vm)
