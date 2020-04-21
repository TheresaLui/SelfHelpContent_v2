<properties
	pageTitle="WSBSnapshotDisappeared"
	description="WSBSnapshotDisappeared"
	infoBubbleText="VSS Snapshot created by WSB disappeared backup"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-wsbsnapshotdisappeared"
	diagnosticScenario="azurebackup-crc-wsbsnapshotdisappeared"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error WSBSnapshotDisappeared

<!--issueDescription-->
We have identified that the VSS Snapshot created by WSB is missing due to insufficient space.
<!--/issueDescription-->

## **Recommended Steps**
During the System State backup operation, to store the WSB backup the disk volume requires 12-15 GB of free space. This operation could also impact the C drive volume. To resolve the storage < 30GB issue:

Ensure the free space available on the scratch folder follows the recommendation listed in this [article](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#whats-the-minimum-size-requirement-for-the-cache-folder) and then retry the operation
