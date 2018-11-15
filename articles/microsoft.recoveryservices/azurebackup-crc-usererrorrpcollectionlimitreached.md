<properties
	pageTitle="usererrorrpcollectionlimitreached"
	description="usererrorrpcollectionlimitreached"
	infoBubbleText="The Restore Point collection maximum limit has reached. See details on the right"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	articleId="azurebackup-crc-usererrorrpcollectionlimitreached"
	diagnosticScenario="azurebackup-crc-usererrorrpcollectionlimitreached"
	selfHelpType="diagnostics"
	supportTopicIds="32553276,32553277"
	productPesIds="15207"
	cloudEnvironments="public"
/>

# UserErrorRpCollectionLimitReached
<!--issueDescription-->
We identified that your backup operation was failing due the existence of a lock on the recovery point resource group. 
<!--/issueDescription-->

## **Recommended Steps**

The lock might have been applied on the recovery point resource group from your end for some security reason. The presence of a lock prevents the execution of automatic cleanup, which can result in the recovery point reaching the maximum limit.

To remove the existing lock and to cleanup the recovery point collection, follow the steps listed in the [article](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorrpcollectionlimitreached---the-restore-point-collection-max-limit-has-reached).
