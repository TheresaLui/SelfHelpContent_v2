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

1. Choose a [Windows image template](https://docs.microsoft.com/azure/azure-stack/azure-stack-marketplace-azure-items#microsoft-virtual-machine-images-and-solution-templates) and [download it from Azure marketplace](https://docs.microsoft.com/azure/azure-stack/azure-stack-download-azure-marketplace-item)
1. Create a [custom image and upload it](https://docs.microsoft.com/azure-stack/operator/azure-stack-add-vm-image) to the marketplace
1. Create a [VM marketplace offer](https://docs.microsoft.com/azure-stack/operator/azure-stack-create-and-publish-marketplace-item).

## **Recommended Documents**

* [Windows Virtual Machines Documentation](https://docs.microsoft.com/azure/virtual-machines/windows/)
* [Make a virtual machine image available in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-vm-image)
* [Considerations for using virtual machines in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-vm-considerations)
