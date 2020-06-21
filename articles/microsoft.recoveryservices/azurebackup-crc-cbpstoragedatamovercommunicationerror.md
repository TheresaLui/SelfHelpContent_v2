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
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error CBPStorageDataMoverCommunicationError

<!--issueDescription-->
We have identified that your backup operation failed because the MARS agent was not able to communicate with Azure Backup service.
<!--/issueDescription-->

## **Recommended Steps**

- Verify that you are connected to the internet and proxy server settings are configured correctly
* Ensure access to internet by following these [steps](https://docs.microsoft.com/azure/backup/backup-configure-vault#verify-internet-access)
- If Proxy is used, ensure details are accurate. If not used, remove the settings. To learn more, see this [article](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#verifying-proxy-settings-for-windows).
- If you are using antivirus software then it might interfere with communication and the backup operation. Follow these [steps](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-slow-backup-performance-issue#cause-another-process-or-antivirus-software-interfering-with-azure-backup) to troubleshoot and resolve.
- Retry the operation
