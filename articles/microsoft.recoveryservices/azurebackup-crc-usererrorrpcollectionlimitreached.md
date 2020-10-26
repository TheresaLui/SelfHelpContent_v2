<properties
	pageTitle="usererrorrpcollectionlimitreached"
	description="usererrorrpcollectionlimitreached"
	infoBubbleText="The Restore Point collection maximum limit has reached. See details on the right"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	articleId="azurebackup-crc-usererrorrpcollectionlimitreached"
	diagnosticScenario="AzureBackup_ScenarioLevelInsight"
	selfHelpType="diagnostics"
	supportTopicIds="32553276,32553277"
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# UserErrorRpCollectionLimitReached
<!--issueDescription-->
We identified that your backup operation was failing due the presence of a lock on the recovery point resource group. The lock might have been applied by an authorized user for security reasons. The presence of a lock prevents the execution of automatic cleanup, which can result in the recovery point reaching the maximum limit.
<!--/issueDescription-->

## **Recommended Steps**

4 out of 5 customers resolved their backup failures by following these steps:<br>
Step 1: [Remove the lock from the resource Group](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#remove_lock_from_the_recovery_point_resource_group)<br>
Step 2: [Clean up Restore point collection](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#clean_up_restore_point_collection)<br>

- Backup service creates a separate resource group than the resource group of the VM to store restore point collection. It is mandatory not to lock the resource group created by the Backup service, [Learn more](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorrpcollectionlimitreached---the-restore-point-collection-max-limit-has-reached)
- The naming format of the resource group created by Backup service is:<br>
```
AzureBackupRG_<\Geo>_<\number>
```
For example: AzureBackupRG_northeurope_1

*Note: If locks are applied at subscription level, then the Resource Group will be locked as well. In this scenario, you should remove the lock from the subscription*
