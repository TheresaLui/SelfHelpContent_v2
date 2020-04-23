<properties
    pageTitle="Azure Stack windows-based virtual machines"
    description="Issues with Windows Based Virtual machines"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32663892"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-vm-windows"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Windows-based virtual machines

You can deploy Windows Server VM images on Azure Stack by adding a Windows-based image into the Azure Stack Marketplace. The easiest way to add a Windows image to Azure Stack is through Marketplace Management. These images have been prepared and tested for compatibility with Azure Stack.

## **Recommended Steps**

1. Add a Windows image by [Download marketplace items from Azure to Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-download-azure-marketplace-item)
2. You can review [Microsoft Virtual Machine Images and Solution Templates](https://docs.microsoft.com/azure/azure-stack/azure-stack-marketplace-azure-items#microsoft-virtual-machine-images-and-solution-templates) in the marketplace

### **Known Issues**

Azure Stack version 1905 includes fixes to storage and compute services. For more information, see [Azure Stack Hotfix 1.1905.3.48](https://support.microsoft.com/help/4510078).

* Queue messages: Messages in a queue expire immediately after creation and tagged for garbage collection. This issue may present in three cases:
    * Retrieval of resources in Azure Resource Manager will fail
    * Usage metric data is not collected and uploaded for processing
    * Customer developed applications fail to retrieve messages

* User image management: Failed user image creation puts the user image service into a bad state:
    * New image creation fails once the service is in this state
    * Deletion of image may fail with the following error "Error: An internal disk management error occurred."

## **Recommended Documents**

* [Windows Virtual Machines Documentation](https://docs.microsoft.com/azure/virtual-machines/windows/)
* [Make a virtual machine image available in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-vm-image)
* [Considerations for using virtual machines in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-vm-considerations)
