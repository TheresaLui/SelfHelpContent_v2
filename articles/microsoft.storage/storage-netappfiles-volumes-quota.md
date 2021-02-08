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

Review the following steps to determine the cause of your NetApp Volumes issue.  

## **Recommended Steps**

1. Any consumed snapshot size counts towards the provisioned space of the volume.
2. The volume does not automatically grow upon becoming completely filled. You must either resize the volume or delete data or snapshots from it to create more space.

## **Recommended Documents**

- [Create an NFS volume for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-create-volumes)<br>
- [Cost model for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-cost-model)<br>
