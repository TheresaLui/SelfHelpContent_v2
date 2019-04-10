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
	cloudEnvironments="public"
/>

# UserErrorKeyVaultPermissionsNotConfigured

<!--issueDescription-->
## **Azure Backup Service does not have sufficient permissions to Key Vault for Backup of Encrypted Virtual Machines.**
<!--/issueDescription-->

## **Recommended Docuemnt**
We identified that your backup operation failed due to the backed up VM that does not have required permission to access the key vault or the key used for encrypting the VM is not a standalone key but part of the certificate that Azure Backup supports.

For the successful backup operation on encrypted VMs, refer [Backup-encrypted VM article](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption#backup-encrypted-vm)
