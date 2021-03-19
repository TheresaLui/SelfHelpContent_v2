
<properties
	pageTitle="Can't access the SMB shares"
	description="Learn how to resolve issues related to SMB connectivity"
	service="microsoft.databox.jobs"
	resource=""
	authors="sunilrsanjeev"
	ms.author="sunir"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32639190"
	resourceTags=""
	productPesIds="16505"
	cloudEnvironments="public,fairfax, usnat, ussec"
    	articleId="32639190"
	ownershipId="StorageMediaEdge_DataBox"
/>

# Data Box - Data copy and validation

**Can't access the SMB shares**

## **Recommended Steps**

* To access the SMB shares for Data Box, type:  net use `\\<IP address of the device>\<share name>` `/u:<user name for the share>`

Depending upon your data format, the share paths are:

* Azure Block blob - `\\<IP-address-of-Data-Box>\<storage-account-name>_BlockBlob`
* Azure Page blob - `\\<IP-address-of-Data-Box>\<storage-account-name>_PageBlob`
* Azure Files - `\\<IP-address-of-Data-Box>\<storage-account-name>_AzFile`

## **Recommended Documents**

* [Data copy using SMB](https://docs.microsoft.com/azure/databox/data-box-deploy-copy-data)
