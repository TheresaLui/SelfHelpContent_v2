<properties
	pageTitle="UserErrorBCMRestoreStorageAccountNotFound"
	description="UserErrorBCMRestoreStorageAccountNotFound"
	infoBubbleText="Storage Account specified for Restore operation doesn't exist."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-usererrorbcmrestorestorageaccountnotfound"
	diagnosticScenario="azurebackup-crc-usererrorbcmrestorestorageaccountnotfound"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorBCMRestoreStorageAccountNotFound

<!--issueDescription-->
We identified that your restore operation failed because the Storage Account specified for restore operation doesn't exist.
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, perform the below:

* Ensure the storage account specified for restore operation exists until restore operation is completed
* If the specified storage account is deleted then use a different storage account and retry the operation

## **Recommended Document**

* [Storage account backups](https://docs.microsoft.com/azure/backup/backup-azure-arm-restore-vms#storage-accounts)
