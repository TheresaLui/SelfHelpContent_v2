<properties
	pageTitle="UserErrorRestoreNotPossibleBecauseLogBackupContainsBulkLoggedChanges"
	description="UserErrorRestoreNotPossibleBecauseLogBackupContainsBulkLoggedChanges"
	infoBubbleText="The log backup used for recovery contains bulk-logged changes. It cannot be used to stop at an arbitrary point in time as per the SQL guidelines."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorrestorenotpossiblebecauselogbackupcontainsbulkloggedchanges"
	diagnosticScenario="azurebackup-crc-usererrorrestorenotpossiblebecauselogbackupcontainsbulkloggedchanges"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorRestoreNotPossibleBecauseLogBackupContainsBulkLoggedChanges

<!--issueDescription-->
We have identified that your restore job failed because a database is in bulk logged recovery mode. When data is between a bulk logged transaction and next log transaction, it cannot be recovered.
<!--/issueDescription-->

## **Recommended Document**
To resolve this issue follow the steps listed in this [article](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#usererrorrestorenotpossiblebecauselogbackupcontainsbulkloggedchanges)
