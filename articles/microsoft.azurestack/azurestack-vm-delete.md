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

## **Recommended Steps**

* To delete a virtual machine (VM) from Azure Stack, find the VM resource in the Azure Stack portal and choose the delete option, or use the corresponding command for [Azure PowerShell](https://docs.microsoft.com/powershell/module/azurerm.compute/remove-azurermvm) or [Azure CLI](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-delete)
* Removing a VM will not automatically remove associated resources such as virtual disks, network interfaces, public IPs etc
* If you wish to remove all resources contained in the same resource group, follow the steps for [Azure Stack Portal](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-quick-windows-portal#clean-up-resources), [Azure PowerShell](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-quick-create-vm-windows-powershell#delete-the-virtual-machine), or [Azure CLI](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-quick-create-vm-windows-cli#clean-up-resources)

### **Known Issues**

* Queue messages: Messages in a queue expire immediately after creation and tagged for garbage collection. This issue may present in three cases:
    * Retrieval of resources in Azure Resource Manager will fail
    * Usage metric data is not collected and uploaded for processing
    * Customer developed applications fail to retrieve messages

* User image management: Failed user image creation puts the user image service into a bad state:
    * New image creation fails once the service is in this state
    * Deletion of image may fail with the following error "Error: An internal disk management error occurred."

## **Recommended Documents**

* [Troubleshooting Azure virtual machines](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/)
* [Considerations for using virtual machines in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-vm-considerations)
