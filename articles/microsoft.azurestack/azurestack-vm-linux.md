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

## **Recommended Steps**

1. Add Linux images from the Azure Marketplace, by using steps in [download marketplace items from Azure to Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-download-azure-marketplace-item)
2. If required, you can prepare your own Linux image by using steps in [create a custom image](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-generic), and additional steps for supported distributions, such as:

    - [CentOS-based Distributions](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-centos)
    - [Debian Linux](https://docs.microsoft.com/azure/virtual-machines/linux/debian-create-upload-vhd)
    - [Red Hat Enterprise Linux](https://docs.microsoft.com/azure/virtual-machines/linux/redhat-create-upload-vhd)
    - [SLES & openSUSE](https://docs.microsoft.com/azure/virtual-machines/linux/suse-create-upload-vhd)
    - [Ubuntu Server](https://docs.microsoft.com/azure/virtual-machines/linux/create-upload-ubuntu)

3. Once you have prepared a custom Linux image, [add your image to the marketplace](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-vm-image)

### **Known Issues**

* Queue messages: Messages in a queue expire immediately after creation and tagged for garbage collection. This issue may present in three cases:
    * Retrieval of resources in Azure Resource Manager will fail
    * Usage metric data is not collected and uploaded for processing
    * Customer developed applications fail to retrieve messages

* User image management: Failed user image creation puts the user image service into a bad state:
    * New image creation fails once the service is in this state
    * Deletion of image may fail with the following error "Error: An internal disk management error occurred."

## **Recommended Documents**

- [Add Linux images to Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-linux)
- [Quickstart: Create a Linux server virtual machine with the Azure Stack portal](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-quick-linux-portal) 
