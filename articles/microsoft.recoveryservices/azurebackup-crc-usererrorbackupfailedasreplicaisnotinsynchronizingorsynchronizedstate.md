<properties
	pageTitle="UserErrorBackupFailedAsReplicaIsNotInSynchronizingOrSynchronizedState"
	description="UserErrorBackupFailedAsReplicaIsNotInSynchronizingOrSynchronizedState"
	infoBubbleText="Cannot take backup from an AlwaysOn Availability Group Secondary Replica because it is not in Synchronizing or Synchronized state."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorbackupfailedasreplicaisnotinsynchronizingorsynchronizedstate"
	diagnosticScenario="azurebackup-crc-usererrorbackupfailedasreplicaisnotinsynchronizingorsynchronizedstate"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorBackupFailedAsReplicaIsNotInSynchronizingOrSynchronizedState

<!--issueDescription-->
We have identified that your log backups have failed due to a current replica of the database that is not in 'Synchronizing State' or 'Synchronized State' with the other nodes of the Availability Group.
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, perform the below:

1. Ensure the Secondary replica can communicate with the Primary replica
2. Ensure the Primary and the Secondary replicas are in either the Synchronizing state or Synchronizing state

## **Recommended Document**		

* [Back up behavior in case of Always on availability groups](https://docs.microsoft.com/azure/backup/backup-azure-sql-database#back-up-behavior-in-case-of-always-on-availability-groups)
