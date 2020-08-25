<properties
	pageTitle="Database Backup Failure due to Operation System Error"
	description="Database Backup Failure due to Operation System Error"
	infoBubbleText="Database Backup Failure due to Operation System Error"
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
	articleId="775981ce-7711-4840-8d51-73aef64ae2b8-azurestorage"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
The error/symptom you see can be due to multiple reasons but commonly caused if SAS token is incorrect.
<!--/issueDescription-->

## **Recommended Steps**

- Verify if the SAS token is not more than 128 characters
- Does the SAS token have a symbol(?) at the beginning when you create a credential? If yes, then we need to remove it.
- Please make sure you are able to connect to the storage account from the current machine using Storage explorer or SSMS
- Make sure the policy assigned to SAS token is not expired. You can create a new policy using Azure storage explorer and create a new SAS token from Azure storage explorer with that policy and alter the credential and try backing up again
- Can also be caused due to proxy server. Please follow below:
	- Execute the following command to enable the winhttp proxy, replacing \<addressofproxy\> with the proxy's address:
	   ```netsh winhttp set proxy <addressofproxy>```
	- Restart SQL Server to pick up the proxy settings
    - Enable traceflag 1819 to enable using a proxy for Backup a. DBCC TRACEON(1819, -1)

## **Recommended Documents**

* ["Cannot OPEN BACKUP device" error seen when backing up Azure SQL Managed Instance to Azure Blob Storage](https://techcommunity.microsoft.com/t5/azure-database-support-blog/8220-cannot-open-backup-device-8221-error-seen-when-backing-up/ba-p/369101)
