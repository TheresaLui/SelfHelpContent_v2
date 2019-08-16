<properties
	pageTitle="Backup failures while using Azure Backup agent"
	description="Common issues during backup of files and folders using Azure Backup agent"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="pvrk"
	ms.author="pvrk"
	displayOrder="26"
	selfHelpType="generic"
	supportTopicIds="32553275"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="MoonCake"
	articleId="fc3023bd-b8cf-4451-a14d-76e1a8ba8c15"
/>

# Backup of files and folders with Azure Backup Agent fails

## **Recommended Steps**

- [Ensure Microsoft Azure Recovery Services (MARS) Agent is up to date before troubleshooting further](https://go.microsoft.com/fwlink/?linkid=229525&clcid=0x409)
- [Ensure there is network connectivity between MARS agent and Azure](https://docs.azure.cn/backup/backup-azure-mars-troubleshoot#the-microsoft-azure-recovery-service-agent-was-unable-to-connect-to-microsoft-azure-backup)
- Ensure Microsoft Azure Recovery Services is running (in Service console). If required restart and retry the operation
- [Check if another process or antivirus software is interfering with Azure Backup](https://docs.azure.cn/backup/backup-azure-troubleshoot-slow-backup-performance-issue#cause-another-process-or-antivirus-software-interfering-with-azure-backup) 
- [Scheduled backup fails, but manual backup works](https://docs.azure.cn/backup/backup-azure-mars-troubleshoot#backups-dont-run-according-to-schedule)
- Ensure your OS has the latest updates
- [Troubleshooting common Azure Backup agent issues](https://docs.azure.cn/backup/backup-azure-mars-troubleshoot)

## **Recommended Documents**

- [Invalid vault credentials provided](https://docs.azure.cn/backup/backup-azure-mars-troubleshoot#invalid-vault-credentials-provided)
- [Failed to download the vault credential file](https://docs.azure.cn/backup/backup-azure-mars-troubleshoot#unable-to-download-vault-credential-file)
- [The Microsoft Azure Recovery Service Agent was unable to connect to Microsoft Azure Backup](https://www.microsoft.com/?ref=aka)
- [(407) Proxy Authentication Required](https://www.microsoft.com/?ref=aka)
- [Failed to set the encryption key for secure backup](https://docs.azure.cn/backup/backup-azure-mars-troubleshoot#failed-to-set-the-encryption-key-for-secure-backups)
- [Activation did not succeed completely but the encryption passphrase was saved to the following file](https://docs.azure.cn/backup/backup-azure-mars-troubleshoot#failed-to-set-the-encryption-key-for-secure-backups)
- [Encryption passphrase not correctly configured](https://docs.azure.cn/backup/backup-azure-mars-troubleshoot#encryption-passphrase-not-correctly-configured)
