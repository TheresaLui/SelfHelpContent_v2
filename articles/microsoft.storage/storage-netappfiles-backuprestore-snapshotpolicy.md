<properties
	pageTitle="Managing Snapshot Policy"
	description="Managing Snapshot Policy"
	service="microsoft.storage"
	resource="storage"
	authors="b-kiudup"
	ms.author="b-kiudup"
	displayOrder=""
	articleId="NetAppVolumesManagingSnapshotPolicy"
	selfHelpType="generic"
	supportTopicIds="32777921"
	resourceTags=""
	productPesIds="16469"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="AzureNetAppFiles"
/>

# Common NetApp Volumes Issues Managing Snapshot Policy

## **Recommended Steps**

1. Make sure that the snapshot policy feature is registered. If you are using this feature for the first time, you need to register the feature first. In Azure PowerShell, enter `Register-AzProviderFeature -ProviderNamespace Microsoft.NetApp -FeatureName ANFSnapshotPolicy`.
2. Make sure that sum of all snapshots including snapshots configured from policy and on demand snapshots does not exceed more than 255, as we have a limit of 255 snapshots per volume. Refer to [Resource Limits for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-resource-limits) for more information.

## **Recommended Documents**

- [Manage snapshot policies by using Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-manage-snapshots#manage-snapshot-policies)<br>
- [Troubleshoot snapshot policy issues](https://docs.microsoft.com/azure/azure-netapp-files/troubleshoot-snapshot-policies)<br>
