<properties
  pagetitle="Troubleshoot and resolve lob Lifecycle Management issues"
  description="Troubleshoot and resolve Blob Lifecycle Management issues"
  service="microsoft.storage"
  resource="storageaccounts"
  ms.author="annayak,broder"
  selfhelptype="Generic"
  supporttopicids="32683730,32691086,32691087"
  resourcetags=""
  productpesids="16459,15629"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="troubleshoot_and_resolve_blob_lifecycle_management_issues"
  ownershipid="StorageMediaEdge_StorageBlobs" />
# Troubleshoot and resolve lob Lifecycle Management issues

## **Recommended Steps**

Most customers resolved their Blob Lifecycle Management issue on their own, using the information below.

### **Lifecycle Management may not have executed as per your expectation**

- [**Page blob types are not supported** and will be ignored during policy execution](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal#sample-rule)
- [**Append blob** type supports tiering only. **Block blob** type supports deletion and tiering.](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts#rule-filters)
- [**New or updated policy** - It could take from **24 to 48 hours** to execute a new or updated policy. We recommend waiting up to 48 hours to see the first batch of data transitions.](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal#faq)
- [**System containers** such as **$logs** (diagnostic logs) and **$web** (static website) are not supported and will be ignored during policy execution.](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal#sample-rule)
- [**Immutable blob policies**](https://docs.microsoft.com/azure/storage/blobs/storage-blob-immutable-storage) [and **Blob Leases** will prevent blobs from being deleted](https://docs.microsoft.com/rest/api/storageservices/lease-blob)
- [**Last Access Time Tracking (Preview)** is only available in these limited Regions](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal#move-data-based-on-last-accessed-date-preview)
- [Make sure you are using a supported **Storage account type**](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal#availability-and-pricing)

### **Common prefixMatch misunderstandings**

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

### **Last Access Time based LCM (Preview)**
- [Last Access Time Tracking is only available in these limited Regions](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal#move-data-based-on-last-accessed-date-preview)
- [Last Access Time tracking is not supported for Azure Data Lake Storage Gen2 accounts](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal#storage-account-support)
- [Setup lifecycle management policy based on Last Access Time](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal#how-last-access-time-tracking-works)