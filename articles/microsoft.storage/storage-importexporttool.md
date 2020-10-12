<properties
	pageTitle="I need help with Import/Export Job"
	description="I need help with Import/Export Job"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="passaree"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32551662"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="21593658-34a6-40b6-b722-0bd2789c59d9"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# I need help with Import/Export Job

## **Recommended steps**
The Import/Export service only works with Blob storage. Max size of a block blob or append blob 50,000 X 4 MB (approx. 195 GB) and Max size of a page blob 1 TB. The tool will fail if the size of the file exceeds the max allowed limits.

1. [Make sure you have met the prerequisites](https://azure.microsoft.com/documentation/articles/storage-import-export-service/#pre-requisites)
2. [Troubleshooting the Azure Import/Export Tool](https://msdn.microsoft.com/library/dn529116.aspx)
3. [Questions? Check the FAQ](https://azure.microsoft.com/documentation/articles/storage-import-export-service/#frequently-asked-questions)


## **Recommended documents**
[How to prepare an Import/Export Job?](http://go.microsoft.com/fwlink/?LinkId=785089)<br>
[Storage Blob Size Limits](https://azure.microsoft.com/documentation/articles/storage-scalability-targets/#scalability-targets-for-blobs-queues-tables-and-files)