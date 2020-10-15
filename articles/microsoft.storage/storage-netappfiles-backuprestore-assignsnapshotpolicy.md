<properties
	pageTitle="Issue assigning Snapshot Policy"
	description="Issue assigning Snapshot Policy"
	service="microsoft.storage"
	resource="storage"
	authors="b-kiudup"
	ms.author="b-kiudup"
	displayOrder=""
	articleId="NetAppVolumesIssueassigningSnapshotPolicy"
	selfHelpType="generic"
	supportTopicIds="32777920"
	resourceTags=""
	productPesIds="16469"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="AzureNetAppFiles"
/>

# Common NetApp Volumes Issues Assigning Snapshot Policy

## **Recommended Steps**
Make sure that the snapshot policy feature is registered.
If you are using this feature for the first time, you need to register the feature first.
Register the feature:
Azure PowerShell
Register-AzProviderFeature -ProviderNamespace Microsoft.NetApp -FeatureName ANFSnapshotPolicy

Make sure that sum of all snapshots including snapshots configured from policy and on demand snapshots does not exceed more than 255 as we have a limit of 255 snapshots per volume

## **Recommended Documents**

- [Manage snapshot policies by using Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-manage-snapshots#manage-snapshot-policies)<br>
- [Troubleshoot snapshot policy issues](https://docs.microsoft.com/azure/azure-netapp-files/troubleshoot-snapshot-policies)<br>
