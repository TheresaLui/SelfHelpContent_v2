<properties
    pageTitle="Azure Stack Virtual Machine Deletion Issues"
    description="Azure Stack Virtual Machine Deletion Issues"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32663893,32663894"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-vm-delete"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Virtual Machine Deletion Issues

Removing a VM will not automatically remove associated resources such as virtual disks, network interfaces, public IPs, and so on. 

4 out of 5 customers resolved their issue using the guides listed below.<br>

## **Recommended Steps**

If you wish to remove all resources contained in the same resource group, use any of these options: 

* [Azure Stack Portal](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-quick-windows-portal#clean-up-resources)
* [Azure PowerShell](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-quick-create-vm-windows-powershell#delete-the-virtual-machine)
* [Azure CLI](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-quick-create-vm-windows-cli#clean-up-resources)

## **Recommended Documents**

* [Delete a VM using Azure PowerShell](https://docs.microsoft.com/powershell/module/azurerm.compute/remove-azurermvm)
* [Delete a VM using Azure CLI](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-delete)
* [Troubleshooting Azure virtual machines](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/)
* [Considerations for using virtual machines in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-vm-considerations)
