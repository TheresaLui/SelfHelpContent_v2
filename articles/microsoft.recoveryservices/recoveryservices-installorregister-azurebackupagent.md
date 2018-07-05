<properties
	pageTitle="Azure Recovery Services Agent installation or registration issues"
	description="Azure Recovery Services Agent installation or registration issues"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="saurabhsensharma"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds="32553287"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Azure Recovery Services Agent installation or registration issues

## **Recommended steps**
- [Ensure there is network connectivity between MARS agent and Azure](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#the-microsoft-azure-recovery-service-agent-was-unable-to-connect-to-microsoft-azure-backup) <br>
- Ensure **system clock** on the protected system is configured to correct time zone <br>
- If you are trying to **re-register your server** to a vault, then <br>
  - Ensure the agent is uninstalled on the server and it is deleted from portal <br> 
  - Use the same passphrase that was initially used for registering the server <br>
- [Invalid vault credentials provided. The file is either corrupted or does not have the latest...](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#invalid-vault-credentials-provided-the-file-is-either-corrupted-or-does-not-have-the-latest-credentials-associated-with-recovery-service) <br>
- [The Microsoft Azure Recovery Service Agent was unable to connect to Microsoft Azure Backup](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#the-microsoft-azure-recovery-service-agent-was-unable-to-connect-to-microsoft-azure-backup) <br>
- [Failed to set the encryption key for secure backups](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#failed-to-set-the-encryption-key-for-secure-backups) <br>
- [The encryption passphrase stored on this computer is not correctly configured](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#failed-to-set-the-encryption-key-for-secure-backups) <br>
- Ensure your OS has the latest updates <br>
