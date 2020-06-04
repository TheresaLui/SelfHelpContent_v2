<properties
	pageTitle="Management/Restore a dropped managed instance database"
	description="Management/Restore a dropped managed instance database"
	service="microsoft.sql"
	resource="servers"
	authors="jovanpop-msft"
	ms.author="jovanpop"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637302"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="30508b1e-3c9c-4509-8feb-a75aec16d19d"
	ownershipId="AzureData_AzureSQLMI"
/>

# Restore a dropped managed instance database (Preview)

Managed Instance takes automatic backups (full backups every week, differential every 12 hours, and log backups every 5-10 min) that you can use to restore accidentally deleted database. This feature is in preview, and it is still not officially supported. Currently, you can use Azure PowerShell library to restore the accidentally deleted database.

## **Recommended Steps**

Try some of the following steps to troubleshoot the issue:

- Make sure that the parameters that you provided to the script are correct (especially a name of the database and the time when it is dropped). Note that dropped datetime is in UTC time zone.
- If you are using [PowerShell script](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Restore-dropped-database-on-Azure-SQL-Managed-Instance/ba-p/386285) to take the dropped time, not that this time might not be accurate and can be up to 5 min after the actual drop time. Adjust the drop time if the restore fails.
- Make sure that you can restore the database on Managed Instance, and that you don't have some limit related to storage size or [number of files in General purpose tier](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Reaching-Azure-disk-storage-limit-on-General-Purpose-Azure-SQL/ba-p/386234).
- Make sure that the account that is performing point-in-time restore has **Write** permission on Managed Instance and **Read** permission on subscription and resource group. The recommended role is [SQL Managed Instance Contributor](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#sql-managed-instance-contributor).

## **Recommended Documents**

- [Automated backups in Managed Instance](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups)
- [Restore a dropped database in Managed Instance](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Restore-dropped-database-on-Azure-SQL-Managed-Instance/ba-p/386285)
- [Troubleshooting Backup/restore issues in Managed Instance](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Troubleshooting-potential-backup-restore-issues-on-Azure-SQL/ba-p/633556)
