
<properties
	pageTitle="Issues with copy at Azure datacenter"
	description="issues with copy at Azure datacenter"
	service="microsoft.importexport.jobs"
	resource=""
	authors="madhurinms"
	ms.author="madhn"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32738673,32738674,32738688"
	resourceTags=""
	productPesIds="17082"
	cloudEnvironments="public,fairfax, usnat, ussec"
	articleId="3"
	ownershipId="StorageMediaEdge_ImportExport"
/>

# Azure Import/Export copy failures

## **Recommended Steps**

* The Microsoft Azure Import/Export service may fail to copy some of your files or parts of a file to the Windows Azure Blob service. Some reasons for failures include:

- Corrupted files
- Damaged drives
- The storage account key changed while the file was being transferred

You can run the Microsoft Azure Import/Export Tool with the import job's copy log files, and the tool uploads the missing files (or parts of a file) to your Windows Azure storage account to complete the import job.

## **Recommended Documents**

* [Repairing an import job](https://docs.microsoft.com/azure/storage/common/storage-import-export-tool-repairing-an-import-job-v1)
* [Repairing an export job](https://docs.microsoft.com/azure/storage/common/storage-import-export-tool-repairing-an-export-job-v1?toc=/azure/storage/blobs/toc.json)<br>
* [FAQ](https://docs.microsoft.com/azure/storage/common/storage-import-export-service-faq?toc=/azure/storage/blobs/toc.json#miscellaneous)<br>
