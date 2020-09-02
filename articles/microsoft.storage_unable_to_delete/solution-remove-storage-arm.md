<properties
    pageTitle="Blob Active Lease"
    description="Blob Active Lease"
    service="microsoft.storage"
    resource="storageAccounts"
    authors="JRMayberry"
    ms.author="rimayber"
    displayOrder=""
    selfHelpType="TSG_Content"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="bd3202f5-9c4e-4406-9108-0745834621c3"
    ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Storage Account with Active Lease objects
<!--issueDescription-->
We've researched your case and believe the issue is due to one or more blobs have an existing lease. This commonly happens when Disks are still attached to an Azure VM. In this scenario, the VM will hold a lease on a specific blob, preventing deletion.
<!--/issueDescription-->

## **Recommended Steps**

In order to resolve the issue, please follow the steps detailed on the following [article](https://docs.microsoft.com/en-us/azure/virtual-machines/troubleshooting/storage-resource-deletion-errors#scenario-3-deleting-storage-account---identify-all-blobs-within-storage-account-that-are-attached-to-vms). In summary, the procedure will cover the following main steps:

[**Step 1**: Identify blob attached to a VM](https://docs.microsoft.com/en-us/azure/virtual-machines/troubleshooting/storage-resource-deletion-errors#scenario-3-deleting-storage-account---identify-all-blobs-within-storage-account-that-are-attached-to-vms)
[**Step 2**: Delete VM to detach OS disk](https://docs.microsoft.com/en-us/azure/virtual-machines/troubleshooting/storage-resource-deletion-errors#step-2-delete-vm-to-detach-os-disk)
[**Step 3**: Detach data disk from the VM](https://docs.microsoft.com/en-us/azure/virtual-machines/troubleshooting/storage-resource-deletion-errors#step-3-detach-data-disk-from-the-vm)

## **Recommended Documents**

1. [Troubleshoot storage resource deletion errors](https://docs.microsoft.com/en-us/azure/virtual-machines/troubleshooting/storage-resource-deletion-errors)
