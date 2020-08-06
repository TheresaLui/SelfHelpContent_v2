<properties
  pagetitle="Long-term backup retention"
  service="microsoft.sql"
  resource="servers"
  ms.author="katmac"
  selfhelptype="Generic"
  supporttopicids="32637272"
  resourcetags=""
  productpesids="16259"
  cloudenvironments="public,blackforest,fairfax,mooncake,ussec,usnat"
  articleid="379ee528-035d-46ef-9db5-db77176467c4"
  ownershipid="AzureData_AzureSQLMI" />
# Long-term backup retention

Microsoft Azure SQL Managed Instance generates [automatic backups](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups) (full backups every week, differential every 12 hours, and log backups every 5-10 minutes) that you can use to [restore a database to a specific point-in-time in the past](https://docs.microsoft.com/azure/sql-database/sql-database-recovery-using-backups#point-in-time-restore) within the retention period or use to [restore accidentally deleted databases](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Restore-dropped-database-on-Azure-SQL-Managed-Instance/ba-p/386285). Backups are kept for 7 days by default and this [period can be increased up to 35 days](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups#how-to-change-the-pitr-backup-retention-period) (10 year long-term retention is not supported at this time). For more information, see [Automated backups](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups). SQL Managed Instance [doesn't support a retention period for longer than 35 days currently](https://docs.microsoft.com/azure/sql-database/sql-database-long-term-backup-retention-configure). There is an [open feedback item for this feature](https://feedback.azure.com/forums/915676-sql-managed-instance/suggestions/37154812-implement-long-term-backup) and you can monitor progress at that link.

## **Recommended Steps**

**Maintain Backups for More than 35 Days** 

Use the following workarounds:

- Create manual [COPY_ONLY backups in SQL Managed Instance](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Native-database-backup-in-Azure-SQL-Managed-Instance/ba-p/386154) and save to blob storage on your own storage account for longer than 35 days
- If the manual backup process consumes the resources on your managed instance, you can restore a database on some other managed instance using either the cross-instance restore feature or the geo-restore feature and then take a manual backup from that managed instance

## **Recommended Documents**

- [Automated backups in Managed Instance](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups)
- [Copy-only backups](https://docs.microsoft.com/sql/relational-databases/backup-restore/copy-only-backups-sql-server)
- [COPY_ONLY backups in Managed Instance](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Native-database-backup-in-Azure-SQL-Managed-Instance/ba-p/386154)
- [Troubleshooting Backup/restore issues in Managed Instance](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Troubleshooting-potential-backup-restore-issues-on-Azure-SQL/ba-p/633556)
