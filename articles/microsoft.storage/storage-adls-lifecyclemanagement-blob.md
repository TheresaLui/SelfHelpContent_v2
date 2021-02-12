<properties
  pagetitle="Troubleshoot and resolve ADLSGen2 Lifecycle Management issues&#xD;"
  description="Azure Data Lake Gen 2 Lifecycle Management"
  service="microsoft.storage"
  resource="storageaccounts"
  ms.author="annayak,broder"
  selfhelptype="Generic"
  supporttopicids="32691063"
  resourcetags=""
  productpesids="16598"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="d0925508-71da-4f54-8846-4ef79be3e154"
  ownershipid="StorageMediaEdge_DataLakeStorageGen2" />
# Troubleshoot and resolve ADLSGen2 Lifecycle Management issues

## **Recommended Steps**

Most customers resolved their ADLSGen2 Lifecycle Management issue on their own, using the steps below.

### **Last Access Time based LCM (Preview)**
- **[Last Access Time tracking is NOT supported for Azure Data Lake Storage Gen2 accounts](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal#storage-account-support)**

### **Lifecycle Management doesn't execute when Storage Firewall is enabled without "Trusted Services" selected**

- [Trusted Microsoft Services](https://docs.microsoft.com/azure/storage/common/storage-network-security#trusted-microsoft-services)

### **Lifecycle Management wouldn't transition file for unsupported account or file type**

- [Storage account supported by Lifecycle Management](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts#storage-account-support)
- [Lifecycle management policies are not supported for ADLSGen2 Premier Tier](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-known-issues#lifecycle-management-policies-1)
- [Lease blob also locks the ADLsGen2 file for write or delete operation hence is not affected by Lifecycle Management](https://docs.microsoft.com/rest/api/storageservices/lease-blob)

### **Lifecycle Management may not have executed as per your expectation**

For successful execution of Lifecycle Management policies on the storage account, refer the following execution and rule criteria to make modifications.

1. New or updated policy - It could take from 24 to 48 hours for executing a new or updated policy. We recommend waiting up to 48 hours to see the first batch of data transition.
2. Wildcard character '_*_' - This doesn't mean _'matches one or more occurrences of any character'_. The character '_*_' is a valid character in a ADLSGen2 file name in Azure Storage. Hence, if added in a rule it means match the blobs with '_*_' in the file name.
3. Wildcard character '?' - This doesn't mean _'match a single occurrence of any character'_. The character '?' is a valid character in a file name in Azure Storage. Hence, if added in a rule it means match the blobs with '?' in the ADLSGen2 file name.
4. prefixMatch with '!=' - The prefixMatch rules only consider positive(=) logical comparison. Therefore negative(!=) logical comparison are ignored.

## **Recommended Documents**

- [Naming and Referencing ADLSGen2 Files](https://docs.microsoft.com/rest/api/storageservices/naming-and-referencing-containers--blobs--and-metadata#blob-names)
- [Policy Rule Filters](https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts#rule-filters)