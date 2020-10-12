<properties
	pageTitle="CBPSourceSnapshotFailedLowDiskSpace"
	description="CBPSourceSnapshotFailedLowDiskSpace"
	infoBubbleText="Backup failed because Azure Backup was unable to create a snapshot for the selected backup volume(s) due to insufficient space."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-cbpsourcesnapshotfailedlowdiskspace"
	diagnosticScenario="azurebackup-crc-cbpsourcesnapshotfailedlowdiskspace"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error CBPSourceSnapshotFailedLowDiskSpace

<!--issueDescription-->
We have identified that your backup operation failed because Azure Backup was unable to create a snapshot for the selected backup volume(s) due to insufficient space.
<!--/issueDescription-->

## **Recommended Steps**

* [Increase the shadow copy storage space on the protected volume](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#increase-shadow-copy-storage)
