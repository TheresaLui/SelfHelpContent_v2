<properties
	pageTitle="AutoProtectionCancelledOrNotValid"
	description="AutoProtectionCancelledOrNotValid"
	infoBubbleText="Auto-protection Intent was either removed or is no more valid"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-autoprotectioncancelledornotvalid"
	diagnosticScenario="azurebackup-crc-autoprotectioncancelledornotvalid"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error AutoProtectionCancelledOrNotValid

<!--issueDescription-->
We have identified that your backup operation failed, due to auto-protection being either removed or invalid. When you enable auto-protection on a SQL instance, Configure Backup jobs run for all the databases in that instance. If you disable auto-protection while the jobs are running, then any in-progress jobs are canceled with this error code.
<!--/issueDescription-->

## **Recommended Steps**

* Review this list of [symptoms](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#symptoms) and their corresponding causes and try to resolve the issue
* Re-enable auto-protection to protect databases

