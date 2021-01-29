<properties
	pageTitle="How to check if the transfer scenario is supported"
	description="How to check if the transfer scenario is supported"
        service="Microsoft.Storage"
        resource="Microsoft.Storage/storageAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="385bad81-6fb2-46bc-98d8-3327fb680d5d"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check if the transfer scenario is supported

## Transfer scenarios

Source | OnPrem | Blob Storage | ADLS Gen2 | File Storage | Amazon S3 Bucket
------------ | ------------- | ---------- | -------- | ------ | --------
OnPrem | NA | Yes | Yes | Yes | No
Blob Storage | Yes | Yes | Yes | Yes | No
ADLS Gen2 Storage | Yes | Yes | Yes | No | No
File Storage | Yes | Yes | No | Yes | No
Amazon S3 Bucket | NA | Yes (from S3 to Blob) | No | No | No

## Authorization methods

Storage type | Supported method of Authorization
------------ | -------------
Blob storage | Azure AD & SAS
ADLS Gen2 storage | Azure AD & SAS
File Storage | SAS only 

***

**Blob-Blob Transfer**

1. You have to append a SAS to each source URL. If you authenticate with AAD, you can omit the SAS token from the destination URL only. 

~~~shell

azcopy cp "https://<source-storage-account-name>.blob.core.windows.net/<container-name>/<blob-path>?<SAS-token>" "https://<destination-storage-account-name>.blob.core.windows.net/<container-name>/<blob-path>"

~~~

**ADLS Gen2 accounts**

1. [Multi-protocol access on Data Lake Storage enables](https://docs.microsoft.com/en-us/azure/storage/blobs/data-lake-storage-multi-protocol-access) you use the same URL syntax (blob.core.windows.net) for accounts that have a hierarchical namespace.
