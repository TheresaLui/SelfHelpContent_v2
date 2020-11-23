
<properties
	pageTitle="Prepare to ship is slow"
	description="Learn about the factors affecting prepare to ship"
	service="microsoft.databox.jobs"
	resource=""
	authors="sunilrsanjeev"
	ms.author="sunir"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32639188"
	resourceTags=""
	productPesIds="16505"
	cloudEnvironments="public,fairfax, usnat, ussec"
    	articleId="32639188"
	ownershipId="StorageMediaEdge_DataBox"
/>

# Data Box - Data copy and validation

**Prepare to ship is slow**

## **Recommended Steps**

You may experience slow speeds during prepare to ship if you have a large number of small files. Avoid using multiple data copy methods (SMB, NFS, REST, data copy service) together as this will lead to duplicate data on the device and cause issues during data upload in Azure.

Running prepare to ship is a mandatory step and the device can be shipped back to the datacenter only when this step completes without any critical errors. If you encounter any issues while copying data to the device or running prepare to ship, refer these articles:

* [Troubleshoot issues related to Data Box](https://docs.microsoft.com/azure/databox/data-box-troubleshoot)
* [Troubleshoot issues related to Data Box Blob Storage](https://docs.microsoft.com/azure/databox/data-box-troubleshoot-rest)
