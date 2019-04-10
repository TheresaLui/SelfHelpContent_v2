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

## **Recommended Steps**
We identified that your backup operation failed due to the backed up VM that does not have required permission to access the key vault or the key used for encrypting the VM is not a standalone key but part of the certificate that Azure Backup supports.

For the successful backup operation on encrypted VMs.

* VM must have permissions to access the key vault. To assign permission to the encrypted VM, refer the Backup Encrypted VM article or PowerShell.
* If the key is not a standalone key and part of the certificate (Managed key) then Azure Backup currently does not supports VMs with managed key.

To verify if the key is a part of certificate (i.e. not a stand alone key) perform the below steps:

* Select **All services**, and search for Key vaults. From the list of key vaults, select the key vault associated with the encrypted VM that needs to be backed up.
* Select **Certificate** and search for the certificate name in one of the versions you can find key identifier like this(https://<KeyVaultName>.vault.azure.net/keys/<CerificateName>/e7ffd5572f8f48aba124165865c96ea0)

## **Recommended Document**
To provide permission, refer [Backup-encrypted VM article](https://docs.microsoft.com/azure/backup/backup-azure-vms-encryption#backup-encrypted-vm)
