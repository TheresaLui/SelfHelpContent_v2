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
	cloudEnvironments="MoonCake"
/>

# I need help with Import/Export Job

## **Recommended steps**
The Import/Export service only works with Blob storage. Max size of a block blob or append blob 50,000 X 4 MB (approx. 195 GB) and Max size of a page blob 1 TB. The tool will fail if the size of the file exceeds the max allowed limits.

1. [Make sure you have met the prerequisites](https://docs.azure.cn/storage/common/storage-import-export-service#pre-requisites)
2. [Troubleshooting the Azure Import/Export Tool](https://docs.azure.cn/storage/common/storage-import-export-tool-troubleshooting-v1)
3. [Questions? Check the FAQ](https://docs.azure.cn/storage/common/storage-import-export-service#frequently-asked-questions)


## **Recommended documents**
[How to prepare an Import/Export Job?](https://docs.azure.cn/storage/common/storage-import-export-service#create-an-import-job-in-the-classic-portal)<br>
[Storage Blob Size Limits](https://docs.azure.cn/storage/common/storage-scalability-targets#scalability-targets-for-blobs-queues-tables-and-files)
