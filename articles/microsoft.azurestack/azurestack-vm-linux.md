<properties
    pageTitle="Azure Stack Linux-Based virtual machines"
    description="Issues with Linux-based virtual machines"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629279"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-vm-linux"
/>

# Azure Stack Linux-Based Virtual Machines

You can deploy Linux virtual machines (VMs) on Azure Stack by adding a Linux-based image into the Azure Stack Marketplace. The easiest way to add a Linux image to Azure Stack is through Marketplace Management.

## **Recommended Steps**

1. Wherever possible, download the images available through Marketplace Management which have been prepared and tested for Azure Stack. Add Linux images from the Azure Marketplace, by using steps to [Download marketplace items from Azure to Azure Stack.](https://docs.microsoft.com/azure/azure-stack/azure-stack-download-azure-marketplace-item)
2. If required, you can prepare your own Linux image using the following instructions:

    - [CentOS-based Distributions](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-centos)
    - [Debian Linux](https://docs.microsoft.com/azure/virtual-machines/linux/debian-create-upload-vhd)
    - [Red Hat Enterprise Linux](https://docs.microsoft.com/azure/virtual-machines/linux/redhat-create-upload-vhd)
    - [SLES & openSUSE](https://docs.microsoft.com/azure/virtual-machines/linux/suse-create-upload-vhd)
    - [Ubuntu Server](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-ubuntu)
    - Other distributions and general advice are documented under [Create a custom image: Generic Steps](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-generic)

3. Once you have prepared a custom Linux image, [add your image to the marketplace](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-vm-image)

## **Recommended Documents**

- [Add Linux images to Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-linux)
- [Quickstart: Create a Linux server virtual machine with the Azure Stack portal](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-quick-linux-portal) 