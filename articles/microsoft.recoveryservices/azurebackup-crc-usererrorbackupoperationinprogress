<properties
	pageTitle="usererrorbackupoperationinprogress"
	description="usererrorbackupoperationinprogress"
	infoBubbleText="Unable to initiate backup as another backup operation is currently in progress."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	authorAlias="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorbackupoperationinprogress"
	diagnosticScenario="azurebackup-crc-usererrorbackupoperationinprogress"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# UserErrorBackupOperationInProgress

<!--issueDescription-->
## **When a backup job is in progress, a new job should not be triggered or scheduled until the current job is complete.**
<!--/issueDescription-->

## **Recommended Steps**
We have identified, your recent backup job failed because there is an existing backup job in progress. You can't start a new backup job until the current job finishes.

Ensure the backup operation currently in progress is completed before triggering or scheduling another backup operations. To check the backup jobs status, perform the below steps:

1. Sign in to Azure portal, click **All services**. Type Recovery Services and click **Recovery Services vaults**. The list of recovery services vaults appears.
2. From the list of recovery services vaults, select a vault in which the backup is configured.
3. On the vault dashboard menu, click **Backup Jobs** it displays all the backup jobs.

	* If a backup job is in progress, wait for it to complete or cancel the backup job.
		* To cancel the backup job right-click on the backup job and click **Cancel** or use [PowerShell](https://docs.microsoft.com/powershell/module/azurerm.backup/stop-azurermbackupjob?view=azurermps-6.13.0&viewFallbackFrom=azurermps-6.12.0). 
	* If you have reconfigured the backup in a different vault, then ensure there are no backup jobs running in the old vault. If it exists then cancel the backup job.
		* To cancel the backup job right-click on the backup job and click **Cancel** or use [PowerShell](https://docs.microsoft.com/powershell/module/azurerm.backup/stop-azurermbackupjob?view=azurermps-6.13.0&viewFallbackFrom=azurermps-6.12.0)

4. Retry backup operation.

## **Recommended Document**

If the scheduled backup operation is taking longer time conflicting with the next backup configuration then review the [Best Practices](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#best-practices), [Backup Performance](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#backup-performance) and [Restore consideration](https://docs.microsoft.com/azure/backup/backup-azure-vms-introduction#restore-considerations).
