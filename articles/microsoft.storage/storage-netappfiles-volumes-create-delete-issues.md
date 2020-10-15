<properties
	pageTitle="Issues with Creating or Deleting a Volume"
	description="Issues with Creating or Deleting a Volume"
	service="microsoft.storage"
	resource="storage"
	authors="b-kelamb"
	ms.author="b-kelamb"
	displayOrder=""
	articleId="NetAppVolumesIssueCreateDelete"
	selfHelpType="generic"
	supportTopicIds="32740756"
	resourceTags=""
	productPesIds="16469"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="AzureNetAppFiles"
/>

# Common NetApp Volumes Issues with Create and Delete

## Problems Creating or Deleting a Volume

1. If you are creating or deleting volumes using the Azure NetApp Files REST API, you may be issuing requests to quickly and are being throttled. Refer to [Throttling Resource Manager Requests](https://docs.microsoft.com/azure/azure-resource-manager/management/request-limits-and-throttling#resource-provider-limits) for limit definitions.
2. If you are having issues deleting a Volume, make sure you have deleted all snapshots that have been created from that volume

## **Recommended Documents**

- [Resource Limits for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-resource-limits)<br>
- [Delegate a subnet to Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-delegate-subnet)<br>
- [Create an SMB volume for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-create-volumes-smb)<br>
- [Create an NFS volume for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-create-volumes)<br>
- [Getting access to Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-create-netapp-account)<br>
- [Quickstart: Set up Azure NetApp Files and create an NFS Volumes](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-quickstart-set-up-account-create-volumes)<br>
