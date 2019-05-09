
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
	cloudEnvironments="public,fairfax"
    articleId=""
/>

# Data Box - Data copy and validation

## **Can't access the SMB shares**

## **Recommended Steps**
net use \\<IP address of the device>\<share name> /u:<user name for the share>

Depending upon your data format, the share paths are as follows:
* Azure Block blob - \\10.126.76.172\devicemanagertest1_BlockBlob
* Azure Page blob - \\10.126.76.172\devicemanagertest1_PageBlob
* Azure Files - \\10.126.76.172\devicemanagertest1_AzFile

## **Recommended Documents**
* [Data copy using SMB](https://docs.microsoft.com/azure/databox/data-box-deploy-copy-data)