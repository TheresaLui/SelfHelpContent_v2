<properties
	pageTitle="UserErrorParentFullBackupMissingRemedialFullNotPossible"
	description="UserErrorParentFullBackupMissingRemedialFullNotPossible"
	infoBubbleText="Azure Backup service is not able to connect to the SQL instance"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorparentfullbackupmissingremedialfullnotpossible"
	diagnosticScenario="azurebackup-crc-usererrorparentfullbackupmissingremedialfullnotpossible"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorParentFullBackupMissingRemedialFullNotPossible

<!--issueDescription-->
We have identified that your Log backup is failing because there is no first ever full backup to start the recovery chain. This error code occurs only on the Secondary Server of Always On Configuration. 
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue follow steps listed below:

* Ensure the Primary Replica is up, running, and protected
* Immediately trigger a Full Backup for this data source through portal. The next scheduled log/diff backup will be auto healed to trigger a Full Backup.
