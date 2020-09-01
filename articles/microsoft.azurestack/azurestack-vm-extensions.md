<properties
    pageTitle="Azure Stack virtual machine (VM) extensions"
    description="Resolve issues with Azure Stack virtual machine (VM) extensions"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32663915,32663916"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-vm-extensions"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack virtual machine (VM) extensions

Azure Virtual Machine (VM) extensions are small applications that provide post-deployment configuration and automation tasks on Azure VMs. They allow you to use existing marketplace images, and then customize them with extensions as part of your deployments.

4 out of 5 customers resolved their issue using the guides listed below.<br>

## **Recommended Steps**

- You can view the available extensions in the VM blade in the Azure Stack Portal, under extensions, or for the full list you can use the CLI tools:

  - [Discovering VM Extensions for Linux](https://docs.microsoft.com/azure/virtual-machines/extensions/features-linux)
  - [Discovering VM Extensions for Windows](https://docs.microsoft.com/azure/virtual-machines/extensions/features-windows)

- You can view additional VM extensions available from [Azure Marketplace items available for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-marketplace-azure-items#virtual-machine-extensions)
- Azure VM extensions can be managed using either the Azure CLI, Azure PowerShell, Azure Resource Manager templates, and the Azure portal
- To handle the extension on the VM, you need the Azure VM agent installed
- You do not need to connect to a VM directly to install or delete the extension, because the Azure extension is managed outside of the VM and integrated into the Azure platform

## **Recommended Documents**

- [Download marketplace items from Azure to Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-download-azure-marketplace-item)
- [Azure Marketplace items available for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-marketplace-azure-items)
- [Azure virtual machine extensions and features](https://docs.microsoft.com/azure/virtual-machines/extensions/overview)