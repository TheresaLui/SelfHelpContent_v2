<properties
  pagetitle="Azure SQL DB recover dropped server or resource group"
  description="Azure SQL Database recover dropped server or resource group"
  ms.author="vtpombei"
  selfhelptype="Apollo"
  supporttopicids=""
  resourcetags=""
  productpesids="13491"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  mappedToBucket="true"
  articleid="ECCB85B2-11A3-43A9-BC3C-ED0799829B59"
  ownershipid="AzureData_AzureSQLDB_BackupRestore" />

# Backup and Restore

## How to restore a database

The Azure SQL Database service automatically backs up all user databases. The [default retention interval](https://docs.microsoft.com/azure/azure-sql/database/automated-backups-overview?tabs=single-database#backup-retention) for these backups is based on the service tier of the database, and you can restore to any point in time during the retention window. If you have configured long term backup retention, you may alternatively restore from one of those backups.

The default retention interval for database backups can be changed, as described in the link above. However, it is not possible to restore an Azure SQL Database *where the delete date is earlier than the retention period,* because the backup files have already been deleted. 

See the relevant section for instructions to perform a database restore using your preferred method.

:::Section Restore a database using the Azure portal:::

### Restore a database using the Azure portal
 
1. Go to the Azure SQL Server where the database was and select the **Deleted databases** blade
2. From the list provided, select the database  
3. On the **Create SQL Database – Restore database** window review the parameters.  
    - Source of the backup: select **Point-in-Time** or **Long-term backup retention**  
    - Restore point (UTC): Only available if restoring from **Point-in-Time**. To restore to the moment the database was deleted, don’t change this value. To restore to the earliest moment in time, specify a fictional moment in time.  
    - Select a backup: Only available if restoring from **Long-term backup retention**. From the drop-down, select from the list of available long-term backups.  
    - Database name: Remember that it needs to be unique  
4. Press the **Review + create** button to review and confirm the parameters and terms that will be used to restore the database  
5. If everything is correct, press the **Create** button  

    More details on the [documentation](https://docs.microsoft.com/azure/azure-sql/database/recovery-using-backups#deleted-database-restore).  

:::Section Restore a database using Powershell:::

### Restore a database using Powershell  

1. View all the deleted databases that can be restored along with the deletion date and the recovery period start date  
2. Change the variables according to your environment  

    ```
   $resourceGroupName = "Resource group name"
   $serverName = "Azure SQL Server name" 

   Get-AzSqlDeletedDatabaseBackup `
     -ResourceGroupName $resourceGroupName `
     -ServerName $serverName 
   ```

3. After confirming that the database is on the list, run the following script. Again, change the variables according to your environment.

   ```
   $resourceGroupName = "Resource group name"
   $serverName = "Azure SQL Server name"
   $deletedDatabaseName = "Source database name"
   $targetDatabaseName = "target database name"
   $pointInTime = "point in time of the source database that will be restored, format: yyyy-MM-ddTHH:mm:ss.fffZ"


   $DeletedDatabase = Get-AzSqlDeletedDatabaseBackup `
      -ResourceGroupName $resourceGroupName `
      -ServerName $serverName `
      -DatabaseName $deletedDatabaseName

   Restore-AzSqlDatabase `
      -FromDeletedDatabaseBackup `
      -DeletionDate $DeletedDatabase.DeletionDate `
      -ResourceGroupName $DeletedDatabase.ResourceGroupName `
      -ServerName $DeletedDatabase.ServerName `
      -TargetDatabaseName $targetDatabaseName `
      -ResourceId $DeletedDatabase.ResourceID `
      -Edition "Standard" `
      -ServiceObjectiveName $serviceobjective `
      -PointInTime $pointInTime #this parameter can be removed to recover the database to the moment it was deleted 
   ```

     More details on the [documentation](https://docs.microsoft.com/powershell/module/az.sql/restore-azsqldatabase?view=azps-5.6.0).  

:::Section Restore a database using Azure CLI:::

### Restore a database using Azure CLI

1. View all the deleted databases that can be restored along with several details
2. Change the parameters values according to your environment:

   ```
   az sql db list-deleted --subscription [subscription ID] --resource-group [Resource Group Name] --server [Server Name]
   ```

3. Confirm that the database is on the list, and change the parameters according to your environment. Proceed to step 4 or 5, depending on your scenario.
4. To recover the database to the moment it was deleted, run this command:

   ```
   az sql db restore --resource-group [resource group name] --server [Azure SQL Server name] --name [deleted database name] -- dest-name [target database name] --deleted-time "[Deletion date]" 
   ```

5. To recover the database to a point in time between the earliest recovery time and when the database was deleted, run this command:

   ```
   az sql db restore --resource-group [resource group name] --server [Azure SQL Server name] --name [deleted database name]  --dest-name [target database name] --deleted-time "[Deletion date]" --time [point in time of the source database that will be restored, format "YYYY-MM-DDTHH:MM:SS"]
   ```

More details on the [documentation](https://docs.microsoft.com/cli/azure/sql/db?view=azure-cli-latest#az_sql_db_restore).
