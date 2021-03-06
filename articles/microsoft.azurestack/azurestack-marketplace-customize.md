<properties
    pageTitle="Customize Azure Stack Hub Marketplace"
    description="Customize Azure Stack Hub Marketplace"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="TobyTu"
    ms.author="mquian"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32663922"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="ebdc2083-706d-401c-b984-f433c12f1e9f"
	ownershipId="StorageMediaEdge_AzureStack_Hub"
/>

# Customize Azure Stack Hub Marketplace

**Known issue**

* If VM extension deployment fails for **Ubuntu Server 20.04 LTS**, follow the resolution steps in [Issues using VM extensions in Python 3-enabled Linux Azure Virtual Machines systems](https://docs.microsoft.com/azure/virtual-machines/extensions/issues-using-vm-extensions-python-3) but skip step 2 because Azure Stack Hub does not have the **Run command** functionality. For more information, see [Azure Stack Hub known issues](https://docs.microsoft.com/azure-stack/operator/known-issues?view=azs-2005#issues-using-vm-extensions-in-ubuntu-server-2004).

## **Recommended Steps**

You can add a custom virtual machine (VM) image to the marketplace and make it available to your users. You can add VM images to the Azure Stack Hub Marketplace through the administrator portal or Windows PowerShell. Use either an image from the global Azure Marketplace as a base for your custom image, or your create your own using Hyper-V.

1. [Create the custom VM image](https://docs.microsoft.com/azure-stack/operator/azure-stack-add-vm-image#step-1-create-the-custom-vm-image)
2. [Upload the VM image to a storage account](https://docs.microsoft.com/azure-stack/operator/azure-stack-add-vm-image#step-2-upload-the-vm-image-to-a-storage-account)
3. [Add the VM image as an Azure Stack Hub operator](https://docs.microsoft.com/azure-stack/operator/azure-stack-add-vm-image#step-3-option-1-add-the-vm-image-as-an-azure-stack-hub-operator-using-the-portal)

Then, [Create and publish the Marketplace item](https://docs.microsoft.com/azure-stack/operator/azure-stack-create-and-publish-marketplace-item).

## **Recommended Documents**

- [Prepare a Red Hat-based virtual machine for Azure Stack Hub](https://docs.microsoft.com/azure-stack/operator/azure-stack-redhat-create-upload-vhd)
