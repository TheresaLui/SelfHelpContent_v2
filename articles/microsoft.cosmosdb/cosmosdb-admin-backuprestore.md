<properties
	pageTitle="CosmosDB Backup and Restore" 
	description="Troubleshoot CosmosDB Backup and Restore related issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32741531,32636825,32748845"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-admin-backuprestore"
	displayOrder="1"
	category="CosmosDB Backup and Restore"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Backup and restore
Most users are able to resolve their Backup and Restore case using the steps below.

## **Recommended Steps**


### **Feb 2021 point-in-time restore public preview limitations**
Currently, the point-in-time restore functionality is in public preview and has the following limitations:
- Only Azure Cosmos DB APIs for SQL and MongoDB are supported for continuous backup. Cassandra, Table, and Gremlin APIs are not yet supported.
- An existing account with default periodic backup policy cannot be converted to use continuous backup mode
- Azure sovereign and Azure Government cloud regions not yet supported
- Accounts with customer-managed keys are not supported to use continuous backup
- Multi-regions write accounts are not supported
- Accounts with Synapse Link enabled are not supported
- The restored account is created in the same region where your source account exists. You can't restore an account into a region where the source account did not exist.
- The restore window is only 30 days and cannot be changed
- The backups are not automatically geo-disaster resistant. You have to explicitly add another region to have resiliency for the account and the backup.
- While a restore is in progress, do not modify or delete the Identity and Access Management (IAM) policies that grant the permissions for the account or change any VNET, firewall configuration
- Azure Cosmos DB API for SQL or MongoDB accounts that create unique index after the container is created are not supported for continuous backup. Only containers that create unique index as a part of the initial container creation are supported. For MongoDB accounts, you create unique index using extension commands.
- The point-in-time restore functionality always restores to a new Azure Cosmos account. Restoring to an existing account is currently not supported. If you're interested in providing feedback about in-place restore, contact the Azure Cosmos DB team via your account representative or UserVoice.
- All of the new APIs exposed for listing `RestorableDatabaseAccount`, `RestorableSqlDatabases`, `RestorableSqlContainer`, `RestorableMongodbDatabase`, and `RestorableMongodbCollection` are subject to changes while the feature is in preview.
- After restoring, it is possible that for certain collections, the consistent index may be rebuilding. You can check the status of the rebuild operation via the `IndexTransformationProgress` property.
- The restore process restores all the properties of a container including its TTL configuration. As a result, it is possible that the data restored is deleted immediately if you configured that way. In order to prevent this situation, the restore timestamp must be before the TTL properties were added into the container.



### **Changing backup interval and retention period**
Azure Cosmos DB automatically takes a backup of your data every 4 hours. Additionally, at any point of time, the latest two backups are stored. This configuration is the default and is offered without any additional cost. You can change the default backup interval and retention period during the Azure Cosmos account creation or after the account is created. The backup configuration is set at the Azure Cosmos account level; you need to configure it on each account. After you configure the backup options for an account, it is applied to all the containers within that account. Currently, you can change the backup options from the Azure portal only.  

If the number of copies end up being more than 2, you will be charged for those additional copies. See the Consumed Storage section in the [Pricing page](https://azure.microsoft.com/pricing/details/cosmos-db/) to know the exact price for additional copies.

If you would like to change the default backup options for an existing Azure Cosmos account, see the link [Backup interval and retention period](https://docs.microsoft.com/azure/cosmos-db/online-backup-and-restore#backup-interval-and-retention-period) to change your backup retention using Azure Portal.   

![Backup Retention visual](https://docs.microsoft.com/azure/cosmos-db/media/online-backup-and-restore/configure-backup-interval-retention.png)   

To guarantee low latency, the snapshot of your backup is stored in Azure Blob storage in the same region as the current write region. (If you have a multi-master configuration, it's stored in one of the write regions.) For resiliency against regional disaster, each snapshot of the backup data in Azure Blob storage is again replicated to another region through geo-redundant storage (GRS). The region to which the backup is replicated is based on your source region and the regional pair associated with the source region. You cannot access this backup directly. Azure Cosmos DB team will restore your backup when you request through a support request.  


<br>

### **Requesting a restore**
If you have accidentally delete or corrupt your data, before you create a support request to restore the data, make sure to increase the backup retention for your account to at least seven days. It is best to increase your retention within 8 hours of this event. This way, the Azure Cosmos DB team has enough time to restore your account.

The restore process always creates a new Azure Cosmos account to hold the restored data. The name of the new account, if not specified, will have the format `<Azure_Cosmos_account_original_name>-restored1`. The last digit is incremented if multiple restores are attempted. You cannot restore data to a pre-created Azure Cosmos account.  

Microsoft can only do a copy of a Cosmos DB account within the same subscription and resource group. It is not possible to restore the database to a new subscription. If you need a copy of your data in a new subscription, use the [Cosmos DB Data Migration tool](https://azure.microsoft.com/updates/documentdb-data-migration-tool/).  





### **How long a restore takes**
There is no SLA for restore timelines.
<br>However, the restore process can be broken down into the following:
* The time to engage the Cosmos DB engineering team to initiate the restore based on the case severity
* The execution for the data restore depends upon the size of the data. As an example, after a restore is initiated for 500 GB of data, the approximate restore time could be about 4 hours.
**Note**:  There is no SLA guarantee. The above times are estimates only.  

 

### **Managing your own backups**
We have some suggestions for how you can clone your Cosmos DB to another Resource Group or even to the same RG to manage your own backups:
* Use the [Cosmos DB Data Migration tool](https://azure.microsoft.com/updates/documentdb-data-migration-tool/). With the Azure Cosmos DB Data Migration tool, you can easily migrate data to Azure Cosmos DB. The Azure Cosmos DB Data Migration tool is an open source solution.
* Use Azure Data Factory (ADF). By using ADF, you can copy data from Azure Cosmos DB (SQL API) to another Azure Cosmos DB (SQL API).



### **Reducing need for backups**
Your Cosmos DB account may not require backup/restore for disaster recovery. Azure Cosmos DB provides [High availability with Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/high-availability) to transparently replicate your data across all the Azure regions associated with your Cosmos account.  

 

## **Recommended Documents**  

[Azure Cosmos DB backup and restore process and policy](https://docs.microsoft.com/azure/cosmos-db/online-backup-and-restore)
<br>This article describes how Azure Cosmos DB performs data backup.  

[Multi-region accounts](https://docs.microsoft.com/azure/cosmos-db/how-to-manage-database-account)
<br>This article describes how to manage various tasks on an Azure Cosmos account using the Azure portal, Azure PowerShell, Azure CLI, and Azure Resource Manager templates.  

[Distribute data globally](https://docs.microsoft.com/azure/cosmos-db/distribute-data-globally)
<br>This article describes the Key benefits of global distribution:
* Build global active-active apps
* Highly responsive apps
* Highly available apps
* Maintain business continuity during regional outages
* Scale read and write throughput globally
* Choose from several well-defined consistency models
