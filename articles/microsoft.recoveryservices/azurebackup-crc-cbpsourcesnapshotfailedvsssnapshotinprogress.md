<properties
	pageTitle="CBPSourceSnapshotFailedVSSSnapshotInProgress"
	description="CBPSourceSnapshotFailedVSSSnapshotInProgress"
	infoBubbleText="Backup failed because the creation of another snapshot is currently in progress"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-cbpsourcesnapshotfailedvsssnapshotinprogress"
	diagnosticScenario="azurebackup-crc-cbpsourcesnapshotfailedvsssnapshotinprogress"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error CBPSourceSnapshotFailedVSSSnapshotInProgress

<!--issueDescription-->
Backup failed because the creation of another snapshot is currently in progress.
<!--/issueDescription-->

We have identified that your backup operation failed because the volume shadow copy service is busy taking another snapshot. This is a transient issue, wait for the process to complete and retry backup operation after sometime.
