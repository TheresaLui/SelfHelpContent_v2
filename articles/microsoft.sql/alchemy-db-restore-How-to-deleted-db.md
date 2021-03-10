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

## How to recover a deleted Azure SQL Database 

The following scenarios are not supported.  
- Recover a deleted Azure SQL server  
- Recover an Azure SQL Database where the delete date is earlier than the retention period. Increasing the retention period now will not help  

## How to recover a deleted Azure SQL Database using Azure portal, Powershell or Azure CLI  

Azure Portal  
1. On Azure Portal go to the Azure SQL Server where the database was and select the 'Deleted databases' blade.  
2. From the list provided click on the database  
3. On the 'Create SQL Database – Restore database' window review the parameters  
    - Select source: Select the source of the backup, 'Point-in-Time' or 'Long-term backup retention'  
    - Restore point (UTC): Only available if restoring from 'Point-in-Time'. To restore to the moment the database was deleted don’t change this value, to restore to a earliest moment in time please specify the moment in time pretended  
    - Select a backup: Only available if restoring from 'Long-term backup retention'. On the drop down there will be a list of the available long-term backups that can be used.  
    - Database name: Remember that it needs to be unique  
4. Press the 'Review + create' button to review and confirm the parameters and terms that will be used to restore the database.  
5. If everything is correct press the 'Create' button  

More details on the [documentation](https://docs.microsoft.com/azure/azure-sql/database/recovery-using-backups#deleted-database-restore).  

## Powershell  

View all the deleted databases that can be restored along with the deletion date and the recovery period start date.  
Change the variables according to your environment.  

```
$resourceGroupName = "Resource group name"
$serverName = "Azure SQL Server name" 

Get-AzSqlDeletedDatabaseBackup `
    -ResourceGroupName $resourceGroupName `
    -ServerName $serverName 
```

After confirming that the database is on the list run the following script, again change the variables according to your environment

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

## Azure CLI

View all the deleted databases that can be restored along with several details
Change the parameters values according to your environment

```
az sql db list-deleted --subscription [subscription ID] --resource-group [Resource Group Name] --server [Server Name]
```

After confirming that the database is on the list run one of the following commands, again change the parameters according to your environment

Recover the database to the moment it was deleted

```
az sql db restore --resource-group [resource group name] --server [Azure SQL Server name] --name [deleted database name] --dest-name [target database name] --deleted-time "[Deletion date]" 
```

Recover the database to a point in time between the earliest recovery time and when the database was deleted

```
az sql db restore --resource-group [resource group name] --server [Azure SQL Server name] --name [deleted database name] --dest-name [target database name] --deleted-time "[Deletion date]" --time [point in time of the source database that will be restored, format "YYYY-MM-DDTHH:MM:SS"]
```

More details on the [documentation](https://docs.microsoft.com/cli/azure/sql/db?view=azure-cli-latest#az_sql_db_restore).
