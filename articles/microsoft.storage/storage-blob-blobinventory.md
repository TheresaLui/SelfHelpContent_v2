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

Most users can resolve Azure Storage blob inventory issues by using the following information.

## **Recommended Steps**

### **Blob inventory (Preview)**

Blob inventory is supported for general-purpose v2 and premium BlockBlobStorage accounts. Storage accounts that have hierarchal namespace enabled (ADLS Gen2) are also supported. During the preview, this feature is currently available in the following regions: 

    France Central
    Canada Central
    Canada East

For the most recent list of supported regions, see our [documentation](https://docs.microsoft.com/azure/storage/blobs/blob-inventory).

Also see [how do I enable blob inventory reports](https://docs.microsoft.com/azure/storage/blobs/blob-inventory#enable-inventory-reports)?

**Note:** A blob inventory run is automatically scheduled every day, and an inventory run can take up to 24 hours to complete. Currently, we do not support setting up custom schedules for blob inventory runs.

Also see [what does my blob inventory output look like?](https://docs.microsoft.com/azure/storage/blobs/blob-inventory#inventory-output)

### **Frequently Reported Issues**

* **Enabling Firewall rules on your storage account may block inventory requests** 

If you enable firewall rules for your storage account, inventory requests may be blocked. You can unblock these requests by providing exceptions for trusted Microsoft services. For more information, see the Exceptions section in [configure firewalls and virtual networks](https://docs.microsoft.com/azure/storage/common/storage-network-security#exceptions).

