<properties
	pageTitle="usererrorbackupoperationinprogress"
	description="usererrorbackupoperationinprogress"
	infoBubbleText="Unable to initiate backup as another backup operation is currently in progress."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorbackupoperationinprogress"
	diagnosticScenario="AzureBackup_ScenarioLevelInsight"
	selfHelpType="diagnostics"
	supportTopicIds="32553276,32553277"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# UserErrorBackupOperationInProgress

<!--issueDescription-->
**When a backup job is in progress, a new job should not be triggered or scheduled until the current job is complete.**
<!--/issueDescription-->

## **Recommended Steps**
We have identified that your recent backup job failed because there is an existing backup job in progress. You cannot start a new backup job until the current job finishes.

Ensure the backup operation currently in progress is completed before triggering or scheduling other backup operations. To check the backup jobs status:

1. Sign in to Azure portal and click **All services**. Type Recovery Services and click **Recovery Services vaults**. The list of recovery services vaults appears.
2. From the list of recovery services vaults, select a vault in which the backup is configured
3. On the vault dashboard menu, click **Backup Jobs** to display all the backup jobs

	* If a backup job is in progress, wait for it to complete or cancel the backup job
	* To cancel the backup job, right-click on the backup job and click **Cancel** or use [PowerShell](https://docs.microsoft.com/powershell/module/azurerm.backup/stop-azurermbackupjob?view=azurermps-6.13.0&viewFallbackFrom=azurermps-6.12.0)
	* If you have reconfigured the backup in a different vault, ensure there are no backup jobs running in the old vault

4. Retry backup operation

## **Recommended Documents**

If the scheduled backup operation is taking longer time conflicting with the next backup configuration, review:

* [Best Practices](https://aka.ms/AB-AA4e56d)
* [Backup Performance](https://aka.ms/AB-AA4ecqb)
* [Restore consideration](https://aka.ms/AB-AA4ecqn)
