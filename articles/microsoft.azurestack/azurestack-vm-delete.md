<properties
    pageTitle="Azure Stack Delete Virtual Machine"
    description="Azure Stack Virtual Machine Deletion Issues"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32630578"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-vm-delete"
/>

# Azure Stack Virtual Machine Deletion Issues

## **Recommended Steps**

- To delete a virtual machine (VM) from Azure Stack, find the VM resource in the Azure Stack portal and choose the delete operations, or use the corresponding [Azure PowerShell](https://docs.microsoft.com/powershell/module/azurerm.compute/remove-azurermvm) or [Azure CLI](https://docs.microsoft.com/cli/azure/vm?view=azure-cli-latest#az-vm-delete)
- Removing a VM will not automatically remove associated resources such as virtual disks, network interfaces, public IPs etc.
- If you wish to remove all resources contained in the same resource group, follow steps using [Azure Stack Portal](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-quick-windows-portal#clean-up-resources), [Azure PowerShell](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-quick-create-vm-windows-powershell#delete-the-virtual-machine), or [Azure CLI](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-quick-create-vm-windows-cli#clean-up-resources)

## **Recommended Documents**

- [Troubleshooting Azure virtual machines](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/)
- [Considerations for using virtual machines in Azure Stack ](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-vm-considerations)