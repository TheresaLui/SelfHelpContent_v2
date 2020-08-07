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
    articleId="dcd33bb0-a83a-4c8b-a64d-6e3a17ff74bd"
    ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Container Active Lease
<!--issueDescription-->
We've researched your case and believe the issue is due to one or more blobs have an existing lease. This commonly happens when Disks are still attached to an Azure VM. In this scenario, the VM will hold a lease on a specific blob, preventing deletion.
<!--/issueDescription-->

## **Recommended Steps**

In order to resolve the issue, please follow the steps detailed on the following [article](https://docs.microsoft.com/en-us/azure/virtual-machines/troubleshooting/storage-resource-deletion-errors#scenario-2-deleting-a-container---identify-all-blobs-within-container-that-are-attached-to-vms). In summary, the procedure will cover the following main steps:

[**Step 1**: Identify blob attached to a VM](https://docs.microsoft.com/en-us/azure/virtual-machines/troubleshooting/storage-resource-deletion-errors#scenario-2-deleting-a-container---identify-all-blobs-within-container-that-are-attached-to-vms)
[**Step 2**: Delete VM to detach OS disk](https://docs.microsoft.com/en-us/azure/virtual-machines/troubleshooting/storage-resource-deletion-errors#step-2-delete-vm-to-detach-os-disk)
[**Step 3**: Detach data disk from the VM](https://docs.microsoft.com/en-us/azure/virtual-machines/troubleshooting/storage-resource-deletion-errors#step-3-detach-data-disk-from-the-vm)

## **Recommended Documents**

1. [Troubleshoot storage resource deletion errors](https://docs.microsoft.com/en-us/azure/virtual-machines/troubleshooting/storage-resource-deletion-errors)
