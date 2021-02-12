<properties
	pageTitle="Issues with volume tags"
	description="Issues with volume tags"
	service="microsoft.storage"
	resource="storage"
	authors="b-kelamb"
	ms.author="b-kelamb"
	displayOrder=""
	articleId="NetAppVolumesIssueTags"
	selfHelpType="generic"
	supportTopicIds="32740759"
	resourceTags=""
	productPesIds="16469"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="AzureNetAppFiles"
/>

# Common NetApp Volumes Issues Resource Tags

## Problems creating a volume with resource tags

Azure NetApp Files supports the use of resource tags with Volumes, but not with snapshots.  If you are having issues with adding resource tags during volume creation, try creating the volume first and then adding tags once the volume create is complete.

## **Recommended Documents**

- [Use tags to organize your Azure resources and management hierarchy](https://docs.microsoft.com/azure/azure-resource-manager/management/tag-resources)<br>
