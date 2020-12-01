<properties
pageTitle="Troubleshoot and resolve Blob Inventory issues"
description="Troubleshoot and resolve Blob Inventory issues"
service="microsoft.storage"
resource="storageaccounts"
authors="annayak"
ms.author="annayak"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32781189"
resourceTags=""
productPesIds="16459"
cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
articleId="Troubleshoot_and_resolve_Blob_Inventory_issues"
ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Troubleshoot and resolve Blob Inventory issues

## **Recommended Steps**

Most customers can resolve Blob Inventory issues by using the following steps.

### **Blob Inventory (Preview)**

Blob Inventory is supported for general purpose v2 and premium block blob storage accounts. Storage Accounts that have hierarchal namespace enabled (ADLS Gen2) are also supported. During the preview, this feature is currently available in the following regions. For the most recent list of supported regions, see our [documentation](https://docs.microsoft.com/azure/storage/blobs/blob-inventory).

    France Central
    Canada Central
    Canada East

[How do I enable Blob Inventory reports?](https://docs.microsoft.com/azure/storage/blobs/blob-inventory#enable-inventory-reports)

**Note:** A Blob Inventory run is automatically scheduled every day, and an inventory run can take up to 24 hours to complete. Currently, we do not support setting up custom schedules for Blob Inventory runs.


[What does my Blob Inventory output look like?](https://docs.microsoft.com/azure/storage/blobs/blob-inventory#inventory-output)

### **Frequently Reported Issues**

* **Enabling Firewall rules on your storage account may block inventory requests.** 

If you enable firewall rules for your storage account, inventory requests may be blocked. You can unblock these requests by providing exceptions for trusted Microsoft services. For more information, see the Exceptions section in [Configure firewalls and virtual networks](https://docs.microsoft.com/azure/storage/common/storage-network-security#exceptions).

