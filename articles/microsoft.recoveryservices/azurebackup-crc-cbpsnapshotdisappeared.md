<properties
	pageTitle="CBPSnapshotDisappeared"
	description="CBPSnapshotDisappeared"
	infoBubbleText="VSS Snapshot created for backup disappeared while backup was in progress."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-cbpsnapshotdisappeared"
	diagnosticScenario="azurebackup-crc-cbpsnapshotdisappeared"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error CBPSnapshotDisappeared

<!--issueDescription-->
We have identified that your backup operation failed because the shadow copy storage space on the protected volume is not sufficient.
<!--/issueDescription-->

## **Recommended Steps**

* [Increase the shadow copy storage space on the protected volume](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot)
