<properties
	pageTitle="ApplicatorSyncError"
	description="ApplicatorSyncError"
	infoBubbleText="DPM could not apply changes on replica. Replication cannot continue."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-applicatorsyncerror"
	diagnosticScenario="azurebackup-crc-applicatorsyncerror"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error ApplicatorSyncError

<!--issueDescription-->
We have identified that your backup operation failed while access system files.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, perform the below steps:

- Check if the Event Log is coinciding with the backup failure for disk corruption issues and resolve the issue if any
- In CBEngine logs, search for the error code 0x80070570. If you find references to this error, the Metadata VHD file might be corrupt.
  - To resolve VHD issue, delete the VHDs from the folder *C:\Program Files\Microsoft Azure Recovery Services Agent\Scratch\VHDs* and retry the backup operation
