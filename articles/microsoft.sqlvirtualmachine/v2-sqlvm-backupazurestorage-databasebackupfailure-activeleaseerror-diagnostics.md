<properties
	pageTitle="Database Backup Failure with Active lease Error"
	description="Database Backup Failure with Active lease Error"
	infoBubbleText="Database Backup Failure with Active lease Error"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat"	
	authors="ujpat"
	displayOrder="1"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds="32740094"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="995ae6e2-dfe9-46a4-9a67-de825f461871-azurestorage"
	ownershipId="AzureData_AzureSQLVM"
/>
# We ran diagnostics on your resource and found an issue 

<!--issueDescription-->
This issue can occur if there was some issue with network while backing up a database to Azure storage.
<!--/issueDescription-->

## **Recommended Steps**
- Identify the files which shows 1 TB or show up as active leases on storage account
- Break the lease of the files from Azure portal/Storage explorer
- Delete the backup file
- Re-initiate the backup if needed


## **Recommended Documents**

* [Delete backup blob files with active leases](https://docs.microsoft.com/sql/relational-databases/backup-restore/deleting-backup-blob-files-with-active-leases?view=sql-server-ver15)



