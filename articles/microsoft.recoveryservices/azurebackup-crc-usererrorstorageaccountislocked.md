<properties
	pageTitle="UserErrorStorageAccountIsLocked"
	description="UserErrorStorageAccountIsLocked"
	infoBubbleText="Backup or restore jobs failed due to storage account being in locked state"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorstorageaccountislocked"
	diagnosticScenario="azurebackup-crc-usererrorstorageaccountislocked"
	selfHelpType="diagnostics"
	supportTopicIds=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# UserErrorStorageAccountIsLocked 

<!--issueDescription-->
Backup or restore jobs failed due to storage account being in locked state.
<!--/issueDescription-->

## **Recommended Steps**

- To resolve this issue, remove the lock on the Storage Account or use delete lock instead of read lock and retry the backup or restore operation, [Learn more](https://docs.microsoft.com/azure/azure-resource-manager/management/lock-resources)
