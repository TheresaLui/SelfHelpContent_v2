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
	cloudEnvironments="public"
/>

# Error UserErrorCannotTakeBackupBasedOnBackupPreference

<!--issueDescription-->
We have identified that your backup operation failed due to mismatch in the node type on which the backup was triggered.
<!--/issueDescription-->

## **Recommended Steps**
* If the backup preference of the Availability Group that is set to **SECONDARY_ONLY** then ensure the node on which backup is taken is also **SECONDARY_ONLY** with the current backup type as Log/CopyOnlyFull
* If the backup preference of the Availability Group set to **PRIMARY** and ensure the node on which backup is also **PRIMARY**.

## **Recommended Document**
To configure backup on secondary replicas for an Always On availability group refer this [article](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/configure-backup-on-availability-replicas-sql-server?view=sql-server-2017).
