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

**We ran diagnostics on your resource and found an issue**


The error/symptom indicates you have configured Snapshots/VM Backup using [Azure Backup](https://docs.microsoft.com/azure/backup/backup-overview) which does not do a [Copy-Only Backup](https://docs.microsoft.com/sql/relational-databases/backup-restore/copy-only-backups-sql-server?view=sql-server-ver15) which can cause your Backups configured through maintenance plan, agent jobs or ad hoc backups to fail.


## **Recommended Steps**

- Make sure Full backup for the database has been taken at least once.
-  To fix this issue, add the following [Registry keys](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#troubleshoot-vm-snapshot-issues) on each of the VMs hosting SQL server instances where VM backups are configured: 	
```[HKEY_LOCAL_MACHINE\SOFTWARE\MICROSOFT\BCDRAGENT] "USEVSSCOPYBACKUP"="TRUE"```

## **Recommended Documents**

* [Troubleshoot VM snapshot issues](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#troubleshoot-vm-snapshot-issues)


