<properties
	pageTitle="Management/Data files, file groups, and partitioning"
	description="Management/Data files, file groups, and partitioning"
	service="microsoft.sql"
	resource="servers"
	authors="jovanpop-msft"
	ms.author="jovanpop"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637250"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="b5751b4a-3d44-46ae-bfa2-eb894e719146"
	ownershipId="AzureData_AzureSQLMI"
/>

# Troubleshoot file/storage issues

Managed Instance enables you to define the amount of storage that you would use for your databases, and you need to monitor your application and ensure that your are not reaching the limits. If you are experiencing issues with storage or files, the following steps might help you to troubleshoot and fix the issues.

## **Recommended Steps**

Try some of the following steps to troubleshoot the issue:

- If you are getting storage limit errors like **Could not allocate a new page for database ... because of insufficient disk space in filegroup ...** try to release some space by using **DBCC SHRINK** command or try to **TRUNCATE** some table that you don't need.
- Check are you reaching the [storage limit](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-resource-limits#instance-level-resource-limits) by querying **master.sys.server_resource_stats** view. If you are not reaching the current instance storage limit, check have you reached the limit in the past because maybe some files are shrunk in the meantime.
- Try to identify some query or process that causes peaks in the storage usage - for example **REBUILD INDEX** that fills the log file, a big ETL process that loads a huge amount of data, etc.
- If you cannot shrink database or remove some data, and your storage limit is below 4TB for Business Critical tier and 8TB for General Purpose tier, you would need to add more storage to the instance. Note that this process is not instant, and it might take up to few hours.
- If you have already reached the 4TB max storage limit of the Business Critical instance try to change tier to General Purpose where you have up to 8TB storage.
- If you have already reached the [max storage limit of the instance](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-resource-limits#instance-level-resource-limits) (for example, 4TB for Business Critical and 8TB for General Purpose tiers), and you have no other options, you might consider moving some databases to another instance by using [cross instance point-in-time restore feature](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Cross-instance-point-in-time-restore-in-Azure-SQL-Database/ba-p/386208) to free some space on the current instance.
- If you are getting the error while you are trying to add file on general purpose instance or restore the database with a large number of files check are you reaching the limit of 280 files per instance by querying `master.sys.master_files`. Try to empty and delete some unnecessary files in other databases.
- If you are getting the error when you are trying to add files on general Purpose instance and you have not reached the 280 files per instance limit, check are you [reaching the internal 35TB limit due to file fragmentation](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Reaching-Azure-disk-storage-limit-on-General-Purpose-Azure-SQL/ba-p/386234). In some specific configuration of file sizes your max file number limit might be lower than 280 per instance due to internal fragmentation, and you would need to remove some files.
- If you are getting the errors related to TEMPDB space usage on General Purpose tier, maybe you are reaching the TEMPDB limit that is 24GB/core. Try to remove some objects from TEMPDB  or optimize queries that are using a lot of memory and causes TEMPDB spills, and if this is not possible, you would need to upgrade your Managed Instance to higher tier that has more cores and TEMPDB space.
- If you are getting the error while trying to add and remove file with the message like "this operation cannot be performed", check is there some conflicting operation such as upgrading service tier, backup, or TDE encryption. In most of the cases you can retry the operation later.
- If you are making some changes in the TEMPDB such as adding or removing the data files, changing the size that either return errors or they are reset after some time, beware that you cannot modify the TEMPDB. TEMPDB is periodically rebuilt as an empty database and your changes are either blocked or reset. If you need some objects in TEMPDB, you can create SQL Agent job that will recreate them either periodically or when the service starts.

## **Recommended Documents**

- [Troubleshooting potential file and storage issues on Managed Instance](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Troubleshooting-potential-file-and-storage-issues-on-Managed/ba-p/664547)
- [Moving databases to another instance using cross-instance point-in-time restore](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Cross-instance-point-in-time-restore-in-Azure-SQL-Database/ba-p/386208)
- [Reaching the internal 35TB limit due to file fragmentation](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Reaching-Azure-disk-storage-limit-on-General-Purpose-Azure-SQL/ba-p/386234)
