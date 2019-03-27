<properties
    pageTitle="Azure Stack Linux-Based virtual machines"
    description=""
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

# Azure Stack Linux-Based virtual machines

You can deploy Linux virtual machines (VMs) on Azure Stack by adding a Linux-based image into the Azure Stack Marketplace. The easiest way to add a Linux image to Azure Stack is through Marketplace Management.

## **Recommended steps**

1. Download Linux images from the Azure Marketplace, use the procedures in the article, [Download marketplace items from Azure to Azure Stack.](https://docs.microsoft.com/azure/azure-stack/azure-stack-download-azure-marketplace-item).<br>
2. Select the Linux images that you want to offer users on your Azure Stack.<br>
3. Wherever possible, download the images available through Marketplace Management which have been prepared and tested for Azure Stack. However, you can prepare your own Linux image using the following instructions:
    - [CentOS-based Distributions](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-centos?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)<br>
    - [Debian Linux](https://docs.microsoft.com/azure/virtual-machines/linux/debian-create-upload-vhd?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)<br>
    - [Red Hat Enterprise Linux](https://docs.microsoft.com/azure/azure-stack/azure-stack-redhat-create-upload-vhd)<br>
    - [SLES & openSUSE](https://docs.microsoft.com/azure/virtual-machines/linux/suse-create-upload-vhd?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)<br>
    - [Ubuntu Server](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-ubuntu?toc=%2fazure%2fvirtual-machines%2flinux%2ftoc.json)<br>
4. If you have prepared your own Linux image, [add your image to the marketplace](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-vm-image).<br>

## **Recommended documents**

[Add Linux images to Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-linux)<br> 
[Quickstart: Create a Linux server virtual machine with the Azure Stack portal](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-quick-linux-portal) 