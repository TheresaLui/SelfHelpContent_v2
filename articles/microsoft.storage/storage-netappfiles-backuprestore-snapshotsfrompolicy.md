<properties
	pageTitle="Issue creating snapshots Snapshot Policy"
	description="Issue creating snapshots Snapshot Policy"
	service="microsoft.storage"
	resource="storage"
	authors="b-kiudup"
	ms.author="b-kiudup"
	displayOrder=""
	articleId="NetAppVolumesIssuecreatingSnapshotsfromPolicy"
	selfHelpType="generic"
	supportTopicIds="32777919"
	resourceTags=""
	productPesIds="16469"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="AzureNetAppFiles"
/>

# Common NetApp Volumes Issues Creating snapshots from Policy

## **Recommended Steps**

1. Make sure that the snapshot policy feature is registered. If you are using this feature for the first time, you need to register the feature first. In Azure PowerShell, enter `Register-AzProviderFeature -ProviderNamespace Microsoft.NetApp -FeatureName ANFSnapshotPolicy`.
2. Make sure that sum of all snapshots including snapshots configured from policy and on demand snapshots does not exceed more than 255, as we have a limit of 255 snapshots per volume. Refer to [Resource Limits for Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-resource-limits) for more information.
3. Also make sure that the policy is enabled from netapp account page

## **Recommended Documents**

- [Manage snapshot policies by using Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-manage-snapshots#manage-snapshot-policies)<br>
- [Troubleshoot snapshot policy issues](https://docs.microsoft.com/azure/azure-netapp-files/troubleshoot-snapshot-policies)<br>
