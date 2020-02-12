<properties
	pageTitle="CBPStorageDataMoverCommunicationError"
	description="CBPStorageDataMoverCommunicationError"
	infoBubbleText="The operation failed because Microsoft Azure Recovery Services Agent was unable to contact Azure Backup service ."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-cbpstoragedatamovercommunicationerror"
	diagnosticScenario="azurebackup-crc-cbpstoragedatamovercommunicationerror"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Error CBPStorageDataMoverCommunicationError

<!--issueDescription-->
We have identified that your backup operation failed because the MARS agent was not able to communicate with Azure Backup service.
<!--/issueDescription-->

## **Recommended Steps**
- Verify your network [connectivity](https://docs.microsoft.com/azure/backup/backup-configure-vault#verify-internet-access)
- If you are using antivirus software then it can interfere with communication and backup. Follow [these](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-slow-backup-performance-issue#cause-another-process-or-antivirus-software-interfering-with-azure-backup) steps troubleshoot and resolve
