<properties
	pageTitle="UserErrorVmVaultLocationMismatch"
	description="UserErrorVmVaultLocationMismatch"
	infoBubbleText="Virtual machine and vault are in different region"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrorvmvaultlocationmismatch"
	diagnosticScenario="azurebackup-crc-usererrorvmvaultlocationmismatch"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorVmVaultLocationMismatch

<!--issueDescription-->
We identified that your backup operation failed because the Virtual Machine and the vault that needs to be backed are in different regions.
<!--/issueDescription-->

## **Recommended Document**
To resolve this issue select a vault which is in the same region as Virtual Machine and retry the operation. For more information on the prerequisites to move Recovery Services vault refer this [article](https://docs.microsoft.com/azure/backup/backup-azure-move-recovery-services-vault#prerequisites-for-moving-recovery-services-vault).
