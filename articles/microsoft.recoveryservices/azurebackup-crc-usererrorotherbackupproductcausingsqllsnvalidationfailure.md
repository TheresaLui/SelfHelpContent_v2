<properties
	pageTitle="UserErrorOtherBackupProductCausingSQLLSNValidationFailure"
	description="UserErrorOtherBackupProductCausingSQLLSNValidationFailure"
	infoBubbleText=" Log chain is broken, as another backup product is taking backups"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrorotherbackupproductcausingsqllsnvalidationfailure"
	diagnosticScenario="azurebackup-crc-usererrorotherbackupproductcausingsqllsnvalidationfailure"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorOtherBackupProductCausingSQLLSNValidationFailure

<!--issueDescription-->
We identified that your backup operation failed the Log chain is broken due to another backup product is taking backups.
<!--/issueDescription-->

## **Recommended Document**
To resolve this issue, perform the below:

- Check if there is another SQL backup product or SQL native backup is conflicting with Azure Backup.  Test by disabling the other backup product and retry the operation.
- If you have configured Azure IaaS VM image backup using Azure Backup service, ensure that VM backup is using VSS copy. The instructions to update USEVSSCOPYBACKUP setting can be found in this [article](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#snapshot-creation).
