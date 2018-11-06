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
The backup operation fails when the Restore Point collection maximum limit has reached.
<!--/issueDescription-->

## **Recommended Steps**
We identified that your backup operation was failing due the lock on the recovery point resource group, preventing automatic cleanup of recovery point from reaching the maximum limit.

* To resolve this issue we recommend you remove the lock on the resource group.<br>
* To remove lock and to cleanup the recovery point collection, follow the steps listed in the [article](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-vm-backup-fails-snapshot-timeout#usererrorrpcollectionlimitreached---the-restore-point-collection-max-limit-has-reached).
