<properties
  pagetitle="Long-term backup retention&#xD;"
  service="microsoft.sql"
  resource="managedinstances"
  ms.author="zhizhwan"
  selfhelptype="Generic"
  supporttopicids="32637272"
  resourcetags=""
  productpesids="16259"
  cloudenvironments="public,blackforest,fairfax,mooncake,ussec,usnat"
  articleid="379ee528-035d-46ef-9db5-db77176467c4"
  ownershipid="AzureData_AzureSQLMI" />
# Long-term backup retention

In Azure SQL Managed Instance, you can configure a long-term backup retention policy (LTR) as a public preview feature. This allows you to automatically retain database backups in separate Azure Blob storage containers for up to 10 years. You can then recover a database using these backups with PowerShell.

**LTR for managed instances is currently available in public preview in Azure Public regions.**

## **Recommended Steps**

You can [configure the long-term retention policies](https://docs.microsoft.com/azure/azure-sql/managed-instance/long-term-backup-retention-configure) from Azure portal or PowerShell. 

### Azure RBAC roles to manage long-term retention
For Get-AzSqlInstanceDatabaseLongTermRetentionBackup and Restore-AzSqlInstanceDatabase, you will need to have one of the following roles:

- Subscription Owner role or
- Managed Instance Contributor role or
- Custom role with the following permissions:
  - Microsoft.Sql/locations/longTermRetentionManagedInstanceBackups/read
  - Microsoft.Sql/locations/longTermRetentionManagedInstances/longTermRetentionManagedInstanceBackups/read
  - Microsoft.Sql/locations/longTermRetentionManagedInstances/longTermRetentionDatabases/longTermRetentionManagedInstanceBackups/read

For Remove-AzSqlInstanceDatabaseLongTermRetentionBackup, you will need to have one of the following roles:

- Subscription Owner role or
- Custom role with the following permission:
  - Microsoft.Sql/locations/longTermRetentionManagedInstances/longTermRetentionDatabases/longTermRetentionManagedInstanceBackups/delete
  Note

**The Managed Instance Contributor role does not have permission to delete LTR backups.**

Azure RBAC permissions could be granted in either subscription or resource group scope. However, to access LTR backups that belong to a dropped instance, the permission must be granted in the subscription scope of that instance.

- Microsoft.Sql/locations/longTermRetentionManagedInstances/longTermRetentionDatabases/longTermRetentionManagedInstanceBackups/delete

## **Recommended Documents**

- [Automated backups in Managed Instance](https://docs.microsoft.com/azure/sql-database/sql-database-automated-backups)
- [Understand long-term backup retention](https://docs.microsoft.com/azure/azure-sql/database/long-term-retention-overview)
- [Troubleshooting Backup/restore issues in Managed Instance](https://techcommunity.microsoft.com/t5/Azure-SQL-Database/Troubleshooting-potential-backup-restore-issues-on-Azure-SQL/ba-p/633556)