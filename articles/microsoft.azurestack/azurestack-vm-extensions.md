<properties
  pagetitle="Azure Stack virtual machine (VM) extensions&#xD;"
  service="microsoft.azurestack"
  resource="azurestack"
  ms.author="mabrigg"
  selfhelptype="Generic"
  supporttopicids="32663915,32663916"
  resourcetags=""
  productpesids="16226"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azurestack-vm-extensions"
  ownershipid="StorageMediaEdge_AzureStack_Hub" />
# Azure Stack virtual machine (VM) extensions

Azure Virtual Machine (VM) extensions are small applications that provide post-deployment configuration and automation tasks on Azure VMs. They allow you to use existing marketplace images, and then customize them with extensions as part of your deployments.

4 out of 5 customers resolved their issue using the guides listed below.<br>

## **Recommended Steps**

 - To view a list extensions available in the Azure Stack Portal, go to the **VM blade** and view the list under **Extensions**. 
     - To view the complete list of VM extensions, use the CLI tools:
        - [Discovering VM Extensions for Linux](https://docs.microsoft.com/azure/virtual-machines/extensions/features-linux)
        - [Discovering VM Extensions for Windows](https://docs.microsoft.com/azure/virtual-machines/extensions/features-windows)
     - To view a list of extensions available on Azure Marketplace, see [Azure Marketplace items available for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-marketplace-azure-items#virtual-machine-extensions)

- To manage Azure VM extensions, use either the Azure CLI, Azure PowerShell, Azure Resource Manager templates, or the Azure portal
- To handle the extension on the VM, you must have the Azure VM agent installed
- To install or delete the extension, you don't need to connect to a VM directly. Azure extensions are managed outside of the VM and are integrated into the Azure platform.
- To prevent your VMs from going into an unresponsive state, update to the latest dependency agent version 9.10.3. For more information, see [Linux Ubuntu VMs in non-responsive state for Service Map Agent](https://techcommunity.microsoft.com/t5/azure-monitor-status/linux-ubuntu-vms-in-non-responsive-state-for-service-map-agent/ba-p/1186350).

## Issues with VMs deployed with SQL Extension

Only a single SQL instance is supported. For more information, see [Automate management with the SQL Server IaaS Agent extension](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-server-iaas-agent-extension-automate-management).

## **Recommended Documents**

- [Download marketplace items from Azure to Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-download-azure-marketplace-item)
- [Azure Marketplace items available for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-marketplace-azure-items)
- [Azure virtual machine extensions and features](https://docs.microsoft.com/azure/virtual-machines/extensions/overview)
