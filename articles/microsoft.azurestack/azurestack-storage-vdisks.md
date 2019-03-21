<properties
    pageTitle="Azure Stack Virtual Disks"
    description="Managing virtual disk storage in Azure Stack"
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629207,32629208"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
    articleId="azurestack-storage-vdisks"
/>

# Azure Stack Virtual Disks

Azure Stack supports the use of both managed and unmanaged virtual disks as virtual machine operating system (OS) or data disks.

**Managed disks** simplify disk management for Azure Stack VMs by managing the storage accounts associated with the virtual disks. You only have to specify the size of disk you need, and Azure Stack creates and manages the disk for you.

**Unmanaged disks** require you to create a storage account to store the disks before creating and attaching them to a virtual machine.

## **Recommended Steps**

1. Determine whether you will use **Managed Disks**, or **Unmanaged Disks** for your VM
2. Follow steps to [create virtual machine disk storage in Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-manage-vm-disks)
3. To improve performance and reduce overall costs, place each VM disk in a separate container under same storage account

## **Recommended documents**

* [Azure Stack VM Disk Best Practice Guidelines](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-manage-vm-disks#best-practice-guidelines)
* [Introduction to Azure managed disks](https://docs.microsoft.com/azure/virtual-machines/windows/managed-disks-overview)
* [Azure Stack Managed Disks: differences and considerations](https://docs.microsoft.com/azure/azure-stack/user/azure-stack-managed-disk-considerations)
* [Manage storage capacity for Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-manage-storage-shares)