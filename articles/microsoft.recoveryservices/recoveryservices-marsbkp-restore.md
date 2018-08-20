<properties
	pageTitle="Files and Folder Backup Restore failures"
	description="Files and Folder Backup Restore failures"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32553296"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Restore of files and folders with Azure Backup Agent fails

## **Recommended Steps**
- [Invalid vault credentials provided. The file is either corrupted or does not have the latest...](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#invalid-vault-credentials-provided-the-file-is-either-corrupted-or-does-not-have-the-latest-credentials-associated-with-recovery-service)<br>
- **The vault credentials provided are different from the vault this server is registered to:** to recover the data to different machine, the Target machine and the Source machine **MUST BE** registered with the **same Recovery Services vault** and must use the **same Vault Credentials key** at the time of restoration.<br>
- [Limitation] The target VM's operating system version must be **greater than or equal to** source VM's operating system version for successful restore.<br>
- If you are trying to restore to alternate location/server, then **use the same passphrase** that was initially used during backup <br>
- How to restore files to: [**original location**](https://docs.microsoft.com/azure/backup/backup-azure-restore-windows-server#use-instant-restore-to-recover-data-to-the-same-machine) (or) [**alternative location**?](https://docs.microsoft.com/azure/backup/backup-azure-restore-windows-server#use-instant-restore-to-restore-data-to-an-alternate-machine)<br>
- [Troubleshooting common restore issues](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot) <br>
