<properties
	pageTitle="Database Backup Failure with Container URL Error"
	description="Database Backup Failure with Container URL Error"
	infoBubbleText="Database Backup Failure with Container URL Error"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat"	
	authors="ujpat"
	displayOrder=""
	selfHelpType="diagnostics"
	supportTopicIds="32740094"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="14ad0c1e-4747-4630-b1fd-8801518f9f03-azurestorage"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
The error/symptom indicates you have disabled the blob public access for the storage account.
<!--/issueDescription-->

## **Recommended Steps**

- To fix this issue, please navigate to Azure Portal --> Storage Account --> Configuration --> "Allow Blob Public Access"


