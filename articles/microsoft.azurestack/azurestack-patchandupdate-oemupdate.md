<properties
    pageTitle="Azure Stack Hub OEM update management"
    description="Azure Stack OEM Update Management"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629271"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="azurestack-patchandupdate-oemupdate"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Azure Stack Hub OEM Update Management

In addition to monthly Azure Stack Hub updates and hotfixes, your Azure Stack Hub hardware vendor will also release original equipment manufacturer (OEM) update packages that include driver and firmware updates. While these updates are delivered as separate packages by your OEM hardware vendor, they are imported, installed, and managed the same way update packages from Microsoft update packages are imported, installed, and managed.

Make sure your OEM package is compatible with the version of Azure Stack Hub you are updating to. If it's not compatible, you will need to perform an OEM package update before running an Azure Stack Hub update. For instructions, see [Apply OEM updates](https://docs.microsoft.com/azure-stack/operator/azure-stack-update-oem).

## **Recommended Steps**

1. Ask your OEM how to be notified of updates
1. To apply OEM updates, follow the process outlined in [Apply OEM updates](https://docs.microsoft.com/azure-stack/operator/azure-stack-update-oem)
1. Complete any prerequisites as needed, such as [configuring the hardware vendor VM](https://docs.microsoft.com/azure-stack/operator/azure-stack-update-oem#configure-hardware-vendor-vm) 
1. If you encounter an issue while applying an OEM update on Azure Stack Hub, refer to your OEM’s [reference material or support contact information](https://docs.microsoft.com/azure-stack/operator/azure-stack-update-oem#oem-contact-information)

## **Recommended Documents**

* [Manage updates in Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-updates)
* [Apply Azure Stack original equipment manufacturer (OEM) updates](https://docs.microsoft.com/azure-stack/operator/azure-stack-update-oem)
* [OEM Update reference material and support contact information](https://docs.microsoft.com/azure-stack/operator/azure-stack-update-oem#oem-contact-information)