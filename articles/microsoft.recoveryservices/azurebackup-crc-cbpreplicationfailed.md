<properties
	pageTitle="CBPReplicationFailed"
	description="CBPReplicationFailed"
	infoBubbleText="Windows Server Backup failed to access some system files. Windows Server Backup error message: %WSBMessage;"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-cbpreplicationfailed"
	diagnosticScenario="azurebackup-crc-cbpreplicationfailed"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error CBPReplicationFailed

<!--issueDescription-->
We have identified that your backup operation failed because Microsoft Azure Recovery Services Agent encountered an unexpected failure while transferring data to Microsoft Azure Backup.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, perform the below steps:

- [Ensure the MARS agent is up to date](https://go.microsoft.com/fwlink/?linkid=229525&clcid=0x409)
- Retry the operation. If the issue is transient, retrying will resolve the issue.
