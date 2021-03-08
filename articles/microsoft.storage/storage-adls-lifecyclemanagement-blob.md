<properties
  pagetitle="Troubleshoot and resolve ADLS Gen2 Lifecycle Management issues"
  description="Azure Data Lake Gen 2 Lifecycle Management"
  service="microsoft.storage"
  resource="storageaccounts"
  ms.author="broder"
  selfhelptype="Generic"
  supporttopicids="32691063"
  resourcetags=""
  productpesids="16598"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="d0925508-71da-4f54-8846-4ef79be3e154"
  ownershipid="StorageMediaEdge_DataLakeStorageGen2" />
# Troubleshoot and resolve ADLS Gen2 Lifecycle Management issues

Most customers resolved their Azure Data Lake Storage Gen 2 (ADLS Gen 2) Lifecycle Management issue on their own, using the following information.

## Recommended Documents

### **Some Lifecycle Management features may not be supported for ADLS Gen 2 storage accounts**
- [Blob storage features available in Azure Data Lake Storage Gen2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-supported-blob-storage-features)

### **Reasons why Lifecycle Management may not have executed as expected**

- [**New or updated policy** - It could take from **24 to 48 hours** to execute a new or updated policy. We recommend waiting up to 48 hours to see the first batch of data transitions.](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal#faq)
- [**Unsupported blob types or actions** will be ignored during policy execution](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal#sample-rule) 
    - [Page blobs are not supported](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal#sample-rule) 
    - [Append blobs support tiering only.](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal#sample-rule) 
- [**System containers** such as **$logs** (diagnostic logs), **$web** (static website), and **$blobchangefeed** are not supported and will be ignored during policy execution.](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal#sample-rule)
- [**Immutable blob policies, legal holds**](https://docs.microsoft.com/azure/storage/blobs/storage-blob-immutable-storage) [and **Blob Leases** will prevent blobs from being deleted](https://docs.microsoft.com/rest/api/storageservices/lease-blob)
- [You are not using a supported **Storage account type**](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal#availability-and-pricing)

### **Common prefix match misunderstandings**

For successful execution of Lifecycle Management policies on the storage account, refer the following execution and rule criteria to make modifications.

1. Wildcard character '_*_' - This doesn't mean _'matches one or more occurrences of any character'_. The character '_*_' is a valid character in a blob name in Azure Storage. Hence, if added in a rule it means match the blobs with '_*_' in the blob name.
2. Wildcard character '?' - This doesn't mean _'match a single occurrence of any character'_. The character '?' is a valid character in a blob name in Azure Storage. Hence, if added in a rule it means match the blobs with '?' in the blob name.
3. prefixMatch with '!=' - The prefixMatch rules only consider positive(=) logical comparison. Therefore negative(!=) logical comparison are ignored.

- [Naming and Referencing Blobs](https://docs.microsoft.com/rest/api/storageservices/naming-and-referencing-containers--blobs--and-metadata#blob-names)
- [Policy Rule Filters](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts#rule-filters)

### **Lifecycle Management doesn't execute when Storage Firewall is enabled without "Trusted Services" selected**

- [Configure firewall and virtual networks Exception](https://docs.microsoft.com/azure/storage/common/storage-network-security#manage-exceptions)
- [Trusted Microsoft Services](https://docs.microsoft.com/azure/storage/common/storage-network-security#trusted-microsoft-services)
- [Storage Firewalls and Virtual Networks](https://docs.microsoft.com/azure/storage/common/storage-network-security)

### **Last Access Time based policies (Preview)**
- [Last Access Time Tracking is only available in these limited Regions](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal#move-data-based-on-last-accessed-date-preview)
- [Setup a Lifecycle Management policy based on Last Access Time](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal#how-last-access-time-tracking-works)
