<properties
	pageTitle="CBPSourceSnapshotFailedVSSRetryableError"
	description="CBPSourceSnapshotFailedVSSRetryableError"
	infoBubbleText="Backup failed because of transient errors in VSS"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-cbpsourcesnapshotfailedvssretryableerror"
	diagnosticScenario="azurebackup-crc-cbpsourcesnapshotfailedvssretryableerror"
	selfHelpType="diagnostics"
	supportTopicIds=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

#  CBPSourceSnapshotFailedVSSRetryableError

<!--issueDescription-->
We have identified that your backup operation failed because of an issue on the VSS service
<!--/issueDescription-->

## **Recommended Steps**

- To resolve this issue, ensure there is no other application (3rd party backup) using the VSS service and retry the operation after sometime <br>
- If issue still persists, restart the VSS service and try again
- To restart VSS (Volume Shadow Copy) service<br>
- Navigate to Services.msc and restart 'Volume Shadow Copy service'

(or)
- From an elevated command prompt, run

  * ```net stop VSS```
  * ```net start VSS```
  
  
