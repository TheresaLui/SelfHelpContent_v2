<properties
	pageTitle="Microsoft Azure Backup Server backup restore fails"
	description="Microsoft Azure Backup Server backup restore fails"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32749573"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="75ad1775-2e7c-4378-b789-b2e138dc2cc8"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure Backup Server VM backup or restore fails

## **Recommended Steps**

**Backup**
- [Ensure Microsoft Azure Recovery Services (MARS) Agent is up to date before troubleshooting further](https://support.microsoft.com/help/4589598/update-for-azure-backup-for-microsoft-azure-recovery-services-agent)
- [Ensure there is network connectivity between MARS agent and Azure](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#the-microsoft-azure-recovery-service-agent-was-unable-to-connect-to-microsoft-azure-backup)
- Ensure Microsoft Azure Recovery Services is running (in Service console). If required restart and retry the operation
- [Ensure 5-10% free volume space is available on scratch folder location](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#whats-the-minimum-size-requirement-for-the-cache-folder) <br>
- [Check if another process or antivirus software is interfering with Azure Backup](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-slow-backup-performance-issue#cause-another-process-or-antivirus-software-interfering-with-azure-backup) 
- [Scheduled backup fails, but manual backup works](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#backups-dont-run-according-to-schedule)
- Ensure your OS has the latest updates
- [Troubleshooting common Azure Backup agent issues](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot)

**Restore**
- [Invalid vault credentials provided: The file is either corrupted or does not have the latest information](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot)
- The vault credentials provided are **different from the vault this server is registered to:** to recover the data to different machine, the Target machine and the Source machine must be registered with the **same Recovery Services vault** and use the **same Vault Credentials key** at the time of restoration
- Known Limitation: The target VM's operating system version must be **greater than or equal to** source VM's operating system version for successful restore
- If you are trying to restore to alternate location/server, **use the same passphrase** that was initially used during backup
- How to restore files to: [**original location**](https://docs.microsoft.com/azure/backup/backup-azure-restore-windows-server#use-instant-restore-to-recover-data-to-the-same-machine) (or) [**alternative location**](https://docs.microsoft.com/azure/backup/backup-azure-restore-windows-server#use-instant-restore-to-restore-data-to-an-alternate-machine)
- [Troubleshooting common restore issues](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot)

## **Recommended Documents**

- [Invalid vault credentials provided](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#invalid-vault-credentials-provided)
- [Failed to download the vault credential file](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#unable-to-download-vault-credential-file)
- [The Microsoft Azure Recovery Service Agent was unable to connect to Microsoft Azure Backup](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#the-microsoft-azure-recovery-service-agent-was-unable-to-connect-to-microsoft-azure-backup)<br>
