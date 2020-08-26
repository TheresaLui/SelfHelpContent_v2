<properties
	pageTitle="Database Backup Failure with Differential Backup Error"
	description="Database Backup Failure with Differential Backup Error"
	infoBubbleText="Database Backup Failure with Differential Backup Error"
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
	articleId="afb2f7b4-2b25-45ce-8f36-8631274e99cf-azurestorage"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
The error/symptom indicates you have configured Snapshots backup at VM level which by default does not do a copy only backup resulting in breaking the LSN chain for your native backups configured on your SQL Server.
<!--/issueDescription-->

## **Recommended Steps**

- To make sure that the native backups don’t get impacted due to other backup applications making LSN updates you can take COPYONLY backups. The copy only backups would not cause impact on LSN of the native backups.
-  To fix this issue, add the following registry keys on each of the VMs hosting SQL server instances and where VM backups are configured and post adding this registry key the native backups should not fail.	
```[HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\BCDRAGENT] "USEVSSCOPYBACKUP"="TRUE"```

## **Recommended Documents**

* [Troubleshoot VM snapshot issues](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#troubleshoot-vm-snapshot-issues)


