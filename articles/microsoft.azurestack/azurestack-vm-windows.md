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

You can deploy Windows Server VM images on Azure Stack by adding a Windows-based image into the Azure Stack Hub Marketplace. The easiest way to add a Windows image to Azure Stack is through Marketplace Management. These images have been prepared and tested for compatibility with Azure Stack.

4 out of 5 customers resolved their issue using the guides listed below.<br>

## **Recommended Steps**

1. Choose a [Windows image](https://docs.microsoft.com/azure/azure-stack/azure-stack-marketplace-azure-items#microsoft-virtual-machine-images-and-solution-templates) and [download it to the Azure Stack Hub Marketplace](https://docs.microsoft.com/azure/azure-stack/azure-stack-download-azure-marketplace-item)
1. For ARM deployments, you can create a [custom image and upload it](https://docs.microsoft.com/azure-stack/operator/azure-stack-add-vm-image) to the marketplace
1. If you upload a custom image, you need to create a [VM marketplace item](https://docs.microsoft.com/azure-stack/operator/azure-stack-create-and-publish-marketplace-item) to make it visible to all tenant users
1. If VM activation is failing, see [Troubleshoot virtual machines](https://docs.microsoft.com/azure-stack/operator/azure-stack-troubleshooting#troubleshoot-virtual-machines-vms)

## **Recommended Documents**

* [Windows Virtual Machines Documentation](https://docs.microsoft.com/azure/virtual-machines/windows/)
* [Make a virtual machine image available in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-add-vm-image)
* [Considerations for using virtual machines in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-vm-considerations)
* [Known Issues: VMs on Azure Stack Hub](https://docs.microsoft.com/azure-stack/user/troubleshoot-vm-known-issues)
