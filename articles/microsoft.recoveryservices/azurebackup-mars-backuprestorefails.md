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

Most customers can resolve backup and restore issues by following these guidelines.
## **Recommended Steps**

### Failed backups 

- [Before troubleshooting, ensure that Microsoft Azure Recovery Services (MARS) Agent is up-to-date](https://support.microsoft.com/help/4589598/update-for-azure-backup-for-microsoft-azure-recovery-services-agent)
- [Verify network connectivity between MARS agent and Azure](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#the-microsoft-azure-recovery-service-agent-was-unable-to-connect-to-microsoft-azure-backup)
- Determine whether Microsoft Azure Recovery Services is running (in Service console). If needed, restart and retry the operation.
- [Make sure that the scratch folder location has at least 5-10% free volume space](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#whats-the-minimum-size-requirement-for-the-cache-folder) <br>
- [Check if another process or antivirus software is interfering with Azure Backup](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-slow-backup-performance-issue#cause-another-process-or-antivirus-software-interfering-with-azure-backup) 
- [If the scheduled backup fails, attempt a manual backup](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#backups-dont-run-according-to-schedule)
- Make sure that your OS has all of the latest updates
- [Troubleshoot these common Azure Backup agent issues](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot)

### Failed restores 

- If you receive this error "Invalid vault credentials provided: The file is either corrupted or does not have the latest information", [see this troubleshooting guide](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot)
- Make sure that the Target and Source machines are registered with the **same Recovery Services vault** and use the **same Vault Credentials key** when recovering the data to a different machine. 
- Make sure that the target VM's operating system is the same or a newer version than the source VM's operating system. This is a known limitation.
- If you are trying to restore to an alternate location/server, use the same passphrase that was initially used during backup
- Review guidelines on [how to restore files to the original location](https://docs.microsoft.com/azure/backup/backup-azure-restore-windows-server#use-instant-restore-to-recover-data-to-the-same-machine) or [how to restore files to an alternative location](https://docs.microsoft.com/azure/backup/backup-azure-restore-windows-server#use-instant-restore-to-restore-data-to-an-alternate-machine)
- See [Troubleshoot common restore issues](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot)

## **Recommended Documents**

- [Invalid vault credentials provided](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#invalid-vault-credentials-provided)
- [Failed to download the vault credential file](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#unable-to-download-vault-credential-file)
- [The Microsoft Azure Recovery Service Agent was unable to connect to Microsoft Azure Backup](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#the-microsoft-azure-recovery-service-agent-was-unable-to-connect-to-microsoft-azure-backup)<br>
