<properties
pageTitle="Troubleshoot and resolve Blob Lifecycle Management issues"
description="Troubleshoot and resolve Blob Lifecycle Management issues"
service="microsoft.storage"
resource="storageaccounts"
authors="annayak"
ms.author="annayak"
displayOrder=""
selfHelpType="generic"
supportTopicIds="32683730,32691086,32691087"
resourceTags=""
productPesIds="16459,15629"
cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
articleId="Troubleshoot_and_resolve_Blob_Lifecycle_Management_issues"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Troubleshoot and resolve lob Lifecycle Management issues

## **Recommended Steps**

Most customers resolved their Blob Lifecycle Management issue on their own, using the steps below.

### **Lifecycle Management doesn't execute when Storage Firewall is enabled without "Trusted Services" selected**

- [Configure firewall and virtual networks Exception](https://docs.microsoft.com/azure/storage/common/storage-network-security#exceptions)
- [Storage Firewalls and Virtual Networks](https://docs.microsoft.com/azure/storage/common/storage-network-security)
- [Trusted Microsoft Services](https://docs.microsoft.com/azure/storage/common/storage-network-security#trusted-microsoft-services)

### **Lifecycle Management wouldn't transition blobs for unsupported account or blob type**

- [Storage account supported by Lifecycle Management](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts#storage-account-support)
- [Only Block blob type is currently supported by Lifecycle Management. Page and Append blob types are not supported](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts#rule-filters)
- [Lease Blob locks a blob for write or delete operation hence is not affected by Lifecycle Management](https://docs.microsoft.com/rest/api/storageservices/lease-blob)

### **Lifecycle Management may not have executed as per your expectation**

For successful execution of Lifecycle Management policies on the storage account, refer the following execution and rule criteria to make modifications.

1. New or updated policy - It could take from 24 to 48 hours for executing a new or updated policy. We recommend waiting up to 48 hours to see the first batch of data transition.
2. Wildcard character '_*_' - This doesn't mean _'matches one or more occurrences of any character'_. The character '_*_' is a valid character in a blob name in Azure Storage. Hence, if added in a rule it means match the blobs with '_*_' in the blob name.
3. Wildcard character '?' - This doesn't mean _'match a single occurrence of any character'_. The character '?' is a valid character in a blob name in Azure Storage. Hence, if added in a rule it means match the blobs with '?' in the blob name.
4. prefixMatch with '!=' - The prefixMatch rules only consider positive(=) logical comparison. Therefore negative(!=) logical comparison are ignored.

## **Recommended Documents**

- [Naming and Referencing Blobs](https://docs.microsoft.com/rest/api/storageservices/naming-and-referencing-containers--blobs--and-metadata#blob-names)
- [Policy Rule Filters](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts#rule-filters)
- [Only Block Blob Type is currently supported by Lifecycle Management](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts#rule-filters)
