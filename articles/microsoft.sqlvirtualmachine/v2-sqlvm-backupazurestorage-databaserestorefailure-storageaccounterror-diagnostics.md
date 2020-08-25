<properties
	pageTitle="Database restore failure with storage account"
	description="Database restore failure with storage account"
	infoBubbleText="Database restore failure with storage account"
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
	articleId="159ff84f-be2f-4056-9bc1-95038a63e43d-azurestorage"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
This issue can occur if you have taken a backup and specified the block size to create the backupset in backup parameters.
<!--/issueDescription-->

## **Recommended Steps**
To solve this error, reissue the `RESTORE` statement with `BLOCKSIZE = 65536`.