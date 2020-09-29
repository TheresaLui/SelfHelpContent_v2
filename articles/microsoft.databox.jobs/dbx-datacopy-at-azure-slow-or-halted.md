
<properties
	pageTitle="Data upload to Azure"
	description="Learn how to resolve issues related to Data copy failed/completed with errors"
	service="microsoft.databox.jobs"
	resource=""
	authors="sunilrsanjeev"
	ms.author="sunir"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32639202"
	resourceTags=""
	productPesIds="16505"
	cloudEnvironments="public,fairfax, usnat, ussec"
    	articleId="32639202"
	ownershipId="StorageMediaEdge_DataBox"
/>

# Recommended Steps
1. For Data Box and Data Box Heavy, you might run into [container or file share size limit errors](https://docs.microsoft.com/azure/databox/data-box-troubleshoot#error_container_or_share_capacity_exceeded). While running Prepare to Ship after data copy to the device is complete, this is indicated as ERROR_CONTAINER_OR_SHARE_CAPACITY_EXCEEDED
2. If the container or file share size limit error was not resolved before sending the device back, data copy at Azure will be stopped
3. In order to proceed with data copy at Azure, enable Large File Shares on the destination storage account(s). See [how to enable and create large file shares](https://docs.microsoft.com/azure/storage/files/storage-files-how-to-create-large-file-share?tabs=azure-portal)
4. Continue to log a support ticket with Microsoft Support so that the copy can be resumed.

**Data copy is slow**: No action is required. Data copy is in progress, check back after few hours.

## **Recommended Documents**

**Troubleshoot errors during data copy**

* [Data Box](https://docs.microsoft.com/azure/databox/data-box-troubleshoot)
* [Data Box Disk](https://docs.microsoft.com/azure/databox/data-box-disk-troubleshoot)
