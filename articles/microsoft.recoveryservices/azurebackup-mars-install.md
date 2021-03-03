<properties
	pageTitle="Azure Recovery Services Agent installation or registration issues"
	description="Azure Recovery Services Agent installation or registration issues"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="4"
	selfHelpType="generic"
	supportTopicIds="32553287"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="9618140e-9906-4cb1-9b6b-5d99941d893a"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure Recovery Services Agent installation or registration issues

## **Recommended Steps**

- [Ensure that the OS is supported and has the latest updates](https://docs.microsoft.com/azure/backup/backup-support-matrix-mars-agent#supported-operating-systems)
- [Ensure that Microsoft Azure Recovery Services (MARS) Agent is up-to-date before troubleshooting further](https://docs.microsoft.com/azure/backup/upgrade-mars-agent)
- [Ensure that there is network connectivity between MARS agent and Azure](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#the-microsoft-azure-recovery-service-agent-was-unable-to-connect-to-microsoft-azure-backup)
- Ensure that the **System Clock** on the protected system is configured to the correct time zone
- If you are trying to **re-register your server** to a vault, then:
  - Ensure the agent is uninstalled on the server and it is deleted from portal
  - Use the same passphrase that was initially used for registering the server
- [Ensure that the server has at least .NET Framework version 4.5.2 or higher](https://www.microsoft.com/download/details.aspx?id=30653)
- [Invalid vault credentials provided: The file is either corrupted or does not have up-to-date information](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#invalid-vault-credentials-provided)
- [Microsoft Azure Recovery Service Agent was unable to connect to Microsoft Azure Backup](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#the-microsoft-azure-recovery-service-agent-was-unable-to-connect-to-microsoft-azure-backup)
- [Failed to set the encryption key for secure backups](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#failed-to-set-the-encryption-key-for-secure-backups)
- [The encryption passphrase stored on this computer is not correctly configured](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#encryption-passphrase-not-correctly-configured)
- **The activation did not complete successfully**: [Make sure that you are not surpassing the supported limit of MARS and MABS registered to a single vault](https://docs.microsoft.com/azure/backup/backup-support-matrix#vault-support)

