<properties
	pageTitle="UserErrorKeyVaultPermissionsNotConfigured"
	description="UserErrorKeyVaultPermissionsNotConfigured"
	infoBubbleText="Azure Backup Service does not have sufficient permissions to Key Vault for Backup of Encrypted Virtual Machines."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
  displayOrder=""
	articleId="azurebackup-crc-usererrorkeyvaultpermissionsnotconfigured"
	diagnosticScenario="azurebackup-crc-usererrorkeyvaultpermissionsnotconfigured"
	selfHelpType="diagnostics"
	supportTopicIds="32553276,32553277,32553297,32553299"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorKeyVaultPermissionsNotConfigured

<!--issueDescription-->
Your backup operation failed because you are trying to backup an encrypted VM that does not have the required permission.
<!--/issueDescription-->

## **Recommended Documents**

- Ensure that the encrypted VM has all the [required permission](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption#provide-permissions)
- [Learn how to backup an encrypted VM](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption#encryption-support)
- If you enable encryption for VMs that are already enabled for backup, you need to [provide Azure Backup with permissions to access the Key Vault](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption#provide-permissions) so that backups can continue without disruption
