
<properties
	pageTitle="Can't access the NFS shares"
	description="Learn how to resolve issues related to NFS connectivity"
	service="microsoft.databox.jobs"
	resource=""
	authors="sunilrsanjeev"
	ms.author="sunir"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32639189"
	resourceTags=""
	productPesIds="16505"
	cloudEnvironments="public,fairfax"
    articleId=""
/>

# Data Box - Data copy and validation

## **Can't access the NFS shares**

## **Recommended Steps**
1. Allow NFS client by adding the client IP on Data Box 
2. use the following command on the host to mount the NFS share on your Data Box device:
sudo mount <Data Box device IP>:/<NFS share on Data Box device> <Path to the folder on local Linux computer>

## **Recommended Documents**
* [Data copy using NFS](https://docs.microsoft.com/azure/databox/data-box-deploy-copy-data-via-nfs)