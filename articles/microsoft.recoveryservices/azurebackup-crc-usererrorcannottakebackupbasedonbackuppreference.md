<properties
	pageTitle="UserErrorCannotTakeBackupBasedOnBackupPreference"
	description="UserErrorCannotTakeBackupBasedOnBackupPreference"
	infoBubbleText="The node on which the backup was triggered cannot take the backup of the requested type."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorcannottakebackupbasedonbackuppreference"
	diagnosticScenario="azurebackup-crc-usererrorcannottakebackupbasedonbackuppreference"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorCannotTakeBackupBasedOnBackupPreference

<!--issueDescription-->
We have identified that your backup operation failed due to a mismatch in the node type on which the backup was triggered.
<!--/issueDescription-->

## **Recommended Steps**

* If the backup preference of the Availability Group is set to **SECONDARY_ONLY**, ensure the node on which backup is taken is also **SECONDARY_ONLY** with the current backup type as Log/CopyOnlyFull
* If the backup preference of the Availability Group set to **PRIMARY**, ensure the node on which backup is taken is also **PRIMARY**

## **Recommended Document**

* [Configure backup on secondary replicas for an Always On availability group](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/configure-backup-on-availability-replicas-sql-server?view=sql-server-2017)
