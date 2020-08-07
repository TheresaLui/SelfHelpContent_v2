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

To remove the existing lock and to cleanup the recovery point collection, follow the steps listed in this [article](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorrpcollectionlimitreached---the-restore-point-collection-max-limit-has-reached).
