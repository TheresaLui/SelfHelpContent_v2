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
- [**34513: Invalid vault credentials provided**. The file is either corrupted or does not have the latest credentials associated with recovery service.](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#invalid-vault-credentials-provided-the-file-is-either-corrupted-or-does-not-have-the-latest-credentials-associated-with-recovery-service)<br>
- **100110: The vault credentials provided are different from the vault this server is registered to**<br>
  - To recover the data to different machine, the Target machine and the Source machine **MUST BE** registered with the **same Recovery Services vault** and must use the **same Vault Credentials key** at the time of restoration.<br>
- [Limitation] The target VM's operating system version must be greater than or equal to source VM's operating system version for successful restore.<br>
- [Limitation] Mountpoint duration is low? upgrading to [latest agent](http://aka.ms/azurebackup_agent) will ensure Mountpoint available for 24hrs. <br>
- How to restore files to: [**original location**](https://docs.microsoft.com/azure/backup/backup-azure-restore-windows-server#use-instant-restore-to-recover-data-to-the-same-machine) (or) [**alternative location**?](https://docs.microsoft.com/azure/backup/backup-azure-restore-windows-server#use-instant-restore-to-restore-data-to-an-alternate-machine)<br>
- [How to restore files and folders from Azure IaaS backup?](https://docs.microsoft.com/azure/backup/backup-azure-vms-automation#restore-files-from-an-azure-vm-backup)<br>
