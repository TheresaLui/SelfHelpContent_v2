<properties
	pageTitle="SSJobFailedOnWSB  "
	description="SSJobFailedOnWSB  "
	infoBubbleText="Unable to perform the operation as Windows Server Backup job failed with error message: %WSBMessage;"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-ssjobfailedonwsb"
	diagnosticScenario="azurebackup-crc-ssjobfailedonwsb"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error SSJobFailedOnWSB  

<!--issueDescription-->
We have identified your backup operation failed because of  interference of any anti-virus. 
<!--/issueDescription-->

## **Recommended steps**
- Ensure VM has the latest backup agent installed
- Ensure all VSS Writer issues are resolved (if any in event log) 
- Anti-virus software if installed can interfere with System State Backup. To verify if anti-virus is the root cause, temporarily disable it and retry the operation. For more information, [see](https://docs.microsoft.com/en-us/azure/backup/backup-azure-troubleshoot-slow-backup-performance-issue#cause-another-process-or-antivirus-software-interfering-with-azure-backup)
