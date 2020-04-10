<properties
	pageTitle="OperationCancelledBecauseConflictingOperationRunningUserError"
	description="OperationCancelledBecauseConflictingOperationRunningUserError"
	infoBubbleText="Operation cancelled as a conflicting operation was already running on the same database."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-operationcancelledbecauseconflictingoperationrunningusererror"
	diagnosticScenario="azurebackup-crc-operationcancelledbecauseconflictingoperationrunningusererror"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error OperationCancelledBecauseConflictingOperationRunningUserError

<!--issueDescription-->
We have identified that the backup operation was cancelled, as it was conflicting with another operation running on the same database.
<!--/issueDescription-->

## **Recommended Steps**

This issues occurs when the triggered adhoc/scheduled job is conflicting with another running operation on the database. To resolve this issue, ensure the below conditions are met:

* If one Full backup is running on the database ensure another Full backup is not triggered
* If one Diff backup is running on the database ensure another Diff backup is not triggered
* If one Log backup is running on the database ensure another Log backup is not triggered
