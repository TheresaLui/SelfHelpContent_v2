<properties
	pageTitle="CBPSourceSnapshotFailed"
	description="CBPSourceSnapshotFailed"
	infoBubbleText="Microsoft Azure Recovery Services Agent was unable to create a snapshot of the selected volume. (0x186C2)"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-cbpsourcesnapshotfailed"
	diagnosticScenario="azurebackup-crc-cbpsourcesnapshotfailed"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error CBPSourceSnapshotFailed

<!--issueDescription-->
We have identified that your backup operation failed because the MARS agent was unable to create a snapshot of the volume due to VSS shadow copy creation failure.
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, perform the following:

* Try restarting Microsoft Software Shadow Copy Provider service from services.msc to see if it resolves the issue
* Ensure Microsoft Software Shadow Copy Provider service is enabled and set to Manual from services.msc
* Check event viewer logs for possible VSS related events and resolve them
* [Check if another process or antivirus software is interfering with Azure Backup](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-slow-backup-performance-issue#cause-another-process-or-antivirus-software-interfering-with-azure-backup)
* [Check if there is a limit set on the Shadow Copy Storage limit](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#increase-shadow-copy-storage)
