<properties
	pageTitle="Files and Folder Backup Restore failures"
	description="Files and Folder Backup Restore failures"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32553296"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="9d7bb66b-c9c0-47fa-bbcf-636e88c8c090"
	ownershipId="StorageMediaEdge_Backup"
/>

# Restore of files and folders with Azure Backup Agent fails

## **Recommended Steps**

- How to restore files to [original location](https://docs.microsoft.com/azure/backup/backup-azure-restore-windows-server#use-instant-restore-to-recover-data-to-the-same-machine) (or) [alternative location](https://docs.microsoft.com/azure/backup/backup-azure-restore-windows-server#use-instant-restore-to-restore-data-to-an-alternate-machine)
- [How can I recover the lost passphrase?](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#can-i-recover-if-i-forgot-my-passphrase)
- [How do I recover if I lost my original machine (where backups were taken)?](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#how-do-i-recover-if-i-lost-my-original-machine-where-backups-were-taken)
- Steps to [re-generate passphrase](https://docs.microsoft.com/azure/backup/backup-azure-manage-mars#re-generate-passphrase)
- [Invalid vault credentials provided: The file is either corrupted or does not have the latest information](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#invalid-vault-credentials-provided)
    - The vault credentials provided are **different from the vault this server is registered with**: to recover the data to different machine, the Target machine and the source machine must be registered with the same Recovery Services vault and use the same Vault Credentials key at the time of restoration 
    - Known Limitation: The target VM's operating system version must be greater than or equal to source VM's operating system version for successful restore
    - If you are trying to restore to alternate location/server, use the same passphrase that was initially used during backup

## **Recommended documents**

- [Troubleshoot restore issues with Azure Backup agent](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#troubleshoot-restore-problems)
- [Troubleshooting common restore issues](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot)
- [Microsoft Azure Recovery Services (MARS) Agent frequently asked questions](https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq)
- [Supported/unsupported configurations for Azure backup using Microsoft Azure Recovery Services (MARS) Agent](https://docs.microsoft.com/azure/backup/backup-support-matrix-mars-agent)
