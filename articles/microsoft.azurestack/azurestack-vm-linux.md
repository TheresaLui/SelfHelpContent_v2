<properties
    pageTitle="Azure Stack Linux-Based virtual machines"
    description="Resolve Issues with Linux-based virtual machines for Azure Stack"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32663891,32663895"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-vm-linux"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Resolve Issues with Linux-based virtual machines for Azure Stack

You can deploy Linux virtual machines (VMs) on Azure Stack by adding a Linux-based image into the Azure Stack Marketplace. The easiest way to add a Linux image to Azure Stack is through Marketplace Management. Wherever possible, download the images available through Marketplace Management. These images have been prepared and tested for Azure Stack.

4 out of 5 customers resolved their issue using the guides listed below.<br>

## **Recommended Steps**

1. Add Linux images from the Azure Marketplace, by using steps in [download marketplace items from Azure to Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-download-azure-marketplace-item)
2. If required, you can prepare your own Linux image by using steps in [create a custom image](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-generic), and additional steps for supported distributions, such as:

    - [CentOS-based Distributions](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-centos)
    - [Debian Linux](https://docs.microsoft.com/azure/virtual-machines/linux/debian-create-upload-vhd)
    - [Red Hat Enterprise Linux](https://docs.microsoft.com/azure/virtual-machines/linux/redhat-create-upload-vhd)
    - [SLES & openSUSE](https://docs.microsoft.com/azure/virtual-machines/linux/suse-create-upload-vhd)
    - [Ubuntu Server](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-ubuntu)

3. Once you have prepared a custom Linux image, you need to [add your image to the marketplace](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-vm-image) to make it visible to all tenant users

## Moving or migrating VMs

- You can find an [overview of moving](https://docs.microsoft.com/azure-stack/user/vm-move-overview) your Azure or local Hyper-V VM to Azure Stack Hub
- For instructions on generalizing and moving your Linux VM, see [Move a generalized VM from on-premises to Azure Stack Hub](https://docs.microsoft.com/azure-stack/user/vm-move-generalized)

## Troubleshooting VMs

- For troubleshooting a VHD that you are moving, see [Verify your VHD](https://docs.microsoft.com/azure-stack/user/vm-move-from-azure?view=azs-2005&tabs=win-spec%2Ccreate-vm-spec#verify-your-vhd)
- For general VM troubleshooting guidance, see [Troubleshoot Windows virtual machines in Azure](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/)

## Azure Stack Hub marketplace item for openSUSE

There is not an Azure Stack Hub Marketplace item for openSUSE. An operator can manually add the item to the Marketplace for their instance.

1. Manually prepare the image. For instructions see [Add Linux images to the Azure Stack Hub Marketplace](https://docs.microsoft.com/azure-stack/operator/azure-stack-linux).
1. Upload the image to offer as a Marketplace item. For instructions see [Prepare a SLES or openSUSE virtual machine](https://docs.microsoft.com/azure/virtual-machines/linux/suse-create-upload-vhd).

## **Recommended Documents**

- [Add Linux images to Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-linux)
- [Quickstart: Create a Linux server virtual machine with the Azure Stack portal](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-quick-linux-portal) 
- [Known Issues: VMs on Azure Stack Hub](https://docs.microsoft.com/azure-stack/user/troubleshoot-vm-known-issues)
