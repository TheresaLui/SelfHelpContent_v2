<properties
	pageTitle="Management/Long-term backup retention in managed instance"
	description="Management/Long-term backup retention in managed instance"
	service="microsoft.sql"
	resource="servers"
	authors="jovanpop-msft"
    ms.author="jovanpop"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637272"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="379ee528-035d-46ef-9db5-db77176467c4"
	ownershipId="AzureData_AzureSQLMI"
/>

# Long-term back up retention in managed instance

Managed Instance takes automatic backups (full backups every week, differential every 12 hours, and log backups every 5-10 min) that you can use to restore a database to some point of time in past within the retention period up to 35 days. For more information, see [Automated backups](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups). [Managed Instance currently doesn't support retention period longer than 35 days](https://docs.microsoft.com/azure/sql-database/sql-database-long-term-backup-retention-configure). There is an open [feedback item for this feature](https://feedback.azure.com/forums/915676-sql-managed-instance/suggestions/37154812-implement-long-term-backup) and you can monitor progress there.

## **Recommended Steps**

If you need to keep backups more than 35 days use the following workarounds:

- Use manual [COPY_ONLY backups in Managed Instance](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Native-database-backup-in-Azure-SQL-Managed-Instance/ba-p/386154) to blob storage to keep backups on your own storage account longer than 35 days.
- If the manual backup process consumes the resources on your instance, you can restore a database on some other instance using cross-instance restore or geo-restore feature and take a manual backup from that instance.

## **Recommended Documents**

- [Automated backups in Managed Instance](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups)
- [Copy-only backups](https://docs.microsoft.com/sql/relational-databases/backup-restore/copy-only-backups-sql-server)
- [COPY_ONLY backups in Managed Instance](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Native-database-backup-in-Azure-SQL-Managed-Instance/ba-p/386154)
- [Troubleshooting Backup/restore issues in Managed Instance](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Troubleshooting-potential-backup-restore-issues-on-Azure-SQL/ba-p/633556)