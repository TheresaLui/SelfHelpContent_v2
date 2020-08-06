<properties
	pageTitle="backup/restore/geo-restore"
	description="backup/restore/geo-restore"
	service="microsoft.sql"
	resource="servers"
	authors="jovanpop-msft"
    ms.author="jovanpop"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637265"
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="e12783f2-bdbe-4e61-a19b-7dc5b905bfa1"
	ownershipId="AzureData_AzureSQLMI"
/>

# Geo-restore

[Geo-Restore](https://docs.microsoft.com/azure/sql-database/sql-database-recovery-using-backups#geo-restore) enables you to take your database from a region even if the entire region is down, and restore it to another instance in different geo-region that is available.

## **Recommended Steps**

If you are experiencing the issues with geo-restore functionality in Managed instance, try some of the following steps:

- Check are the source and target instance under the same subscription because cross-subscription geo-restore is not yet supported.
- Check is there some [known issue](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#Issues) that might cause the problem that you are experiencing.

## **Recommended Documents**

- [Automated backups](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups)
- [Disaster recovery using geo-restore](https://docs.microsoft.com/azure/sql-database/saas-dbpertenant-dr-geo-restore?WT.mc_id=pid:13491:sid:32630425/)<br>
- [Get-AzSqlInstanceDatabaseGeoBackup](https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancedatabasegeobackup) PowerShell command.
- [Restore-AzSqlInstanceDatabase](https://docs.microsoft.com/powershell/module/az.sql/restore-azsqlinstancedatabase) PowerShell command.
- 