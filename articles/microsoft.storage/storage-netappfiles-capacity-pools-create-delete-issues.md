<properties
	pageTitle="Issues with Creating or Deleting a Capacity Pool"
	description="Issues with Creating or Deleting a Capacity Pool"
	service="microsoft.storage"
	resource="storage"
	authors="b-kelamb"
	ms.author="b-kelamb"
	displayOrder=""
	articleId="NetAppCapacityPoolsIssueCreateDelete"
	selfHelpType="generic"
	supportTopicIds="32740754"
	resourceTags=""
	productPesIds="16469"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="AzureNetAppFiles"
/>

# Common NetApp Capacity Pool Issues with Create and Delete

## Problems Deleting a Capacity Pool

If you are having issues deleting a Capacity Pool, make sure that all Azure NetApp Files Volumes and Snapshots in the subscription where you are trying to delete the Capacity Pool have been removed first.  If you have cleaned up all Volumes and Snapshots and still cannot delete the Capacity Pool, it's possible there are still references to resources that are not showing up in the portal.  In this case, continue to file a support ticket, and specify that you have cleaned up all visible Volumes and Snapshots but still cannot delete the Capacity Pool.


## **Recommended Documents**

- [Setting up a Capacity Pool](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-set-up-capacity-pool)<br>
- [Resource Limits for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-resource-limits)<br>
- [Azure NetApp Files Quickstart Guide](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-quickstart-set-up-account-create-volumes)<br>