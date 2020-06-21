<properties
	pageTitle="UserErrorSQLLSNValidationFailure"
	description="UserErrorSQLLSNValidationFailure"
	infoBubbleText="Log chain is broken."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorsqllsnvalidationfailure"
	diagnosticScenario="azurebackup-crc-usererrorsqllsnvalidationfailure"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorSQLLSNValidationFailure

<!--issueDescription-->
We have identified that your backup operation failed due to a conflict with another backup application.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue follow steps listed below:

* Check the steps described in this [article](https://docs.microsoft.com/azure/backup/backup-sql-server-azure-troubleshoot#usererrorsqllsnvalidationfailure) for conflicting backup solutions or log chain issues
* If you have configured both Azure IaaS VM and SQL Server backup, the VM backup creates a VSS full backup causing snapshot task delays. Set the `USEVSSCOPYBACKUP` registry key as described in this [article](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#troubleshoot-vm-snapshot-issues).
