<properties
	pageTitle="Issue with volume quota"
	description="Issue with volume quota"
	service="microsoft.storage"
	resource="storage"
	authors="b-kiudup"
	ms.author="b-kiudup"
	displayOrder=""
	articleId="NetAppVolumesIssuevolumequota"
	selfHelpType="generic"
	supportTopicIds="32784417"
	resourceTags=""
	productPesIds="16469"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="AzureNetAppFiles"
/>

# NetApp Volumes Issue with volume quota or size

## **Recommended Steps**

1. Note that consumed snapshot size counts towards the provisioned space of the volume.
2. Note that the volume does not auto grow upon filling up. Either it has to be resized or some data or snapshots have to be deleted.

## **Recommended Documents**

- [Create an NFS volume for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-create-volumes)<br>
- [Cost model for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-cost-model)<br>
