<properties
	pageTitle="Azure Recovery Services Agent installation or registration issues"
	description="Azure Recovery Services Agent installation or registration issues"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="27"
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="azurebackup-mars-install-mooncake"
	ownershipId="Compute_SiteRecovery"
/>

# Azure Recovery Services Agent installation or registration issues

## **Recommended Steps**

- [Ensure there is network connectivity between MARS agent and Azure](https://docs.azure.cn/backup/backup-azure-mars-troubleshoot#the-microsoft-azure-recovery-service-agent-was-unable-to-connect-to-microsoft-azure-backup)
- Ensure **System Clock** on the protected system is configured to correct time zone
- If you are trying to **reregister your server** to a vault, then:

  - Ensure the agent is uninstalled on the server and it is deleted from portal
  - Use the same passphrase that was initially used for registering the server

- Ensure your OS has the latest updates
- [Ensure that the server has at least .Net Framework version 4.5.2 and higher](https://www.microsoft.com/download/details.aspx?id=30653)
- [Invalid vault credentials provided: The file is either corrupted or does not have the latest information](https://docs.azure.cn/backup/backup-azure-mars-troubleshoot#invalid-vault-credentials-provided)
- [The Microsoft Azure Recovery Service Agent was unable to connect to Microsoft Azure Backup](https://docs.azure.cn/backup/backup-azure-mars-troubleshoot#the-microsoft-azure-recovery-service-agent-was-unable-to-connect-to-microsoft-azure-backup)
- [Failed to set the encryption key for secure backups](https://docs.azure.cn/backup/backup-azure-mars-troubleshoot#failed-to-set-the-encryption-key-for-secure-backups)
- [The encryption passphrase stored on this computer is not correctly configured](https://docs.azure.cn/backup/backup-azure-mars-troubleshoot#encryption-passphrase-not-correctly-configured)
