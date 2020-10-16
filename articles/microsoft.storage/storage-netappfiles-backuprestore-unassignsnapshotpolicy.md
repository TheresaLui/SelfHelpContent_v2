<properties
	pageTitle="Issue unassigning Snapshot Policy"
	description="Issue unassigning Snapshot Policy"
	service="microsoft.storage"
	resource="storage"
	authors="b-kiudup"
	ms.author="b-kiudup"
	displayOrder=""
	articleId="NetAppVolumesIssueunassigningSnapshotPolicy"
	selfHelpType="generic"
	supportTopicIds="32777922"
	resourceTags=""
	productPesIds="16469"
	cloudEnvironments="public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="AzureNetAppFiles"
/>

# Common NetApp Volumes Issues Un-Assigning Snapshot Policy

## **Recommended Steps**
1. Make sure that the snapshot policy feature is registered. If you are using this feature for the first time, you need to register the feature first. In Azure PowerShell, enter `Register-AzProviderFeature -ProviderNamespace Microsoft.NetApp -FeatureName ANFSnapshotPolicy`.
2. Be aware that existing snapshots will not be cleared after removing policy

## **Recommended Documents**

- [Manage snapshot policies by using Azure NetApp Files](https://docs.microsoft.com/azure/azure-netapp-files/azure-netapp-files-manage-snapshots#manage-snapshot-policies)<br>
- [Troubleshoot snapshot policy issues](https://docs.microsoft.com/azure/azure-netapp-files/troubleshoot-snapshot-policies)<br>
