<properties
	pageTitle="CosmosDB Backup and Restore PITR" 
	description="Troubleshoot CosmosDB Backup and Restore PITR"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32787635"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-backuprestore-pitr"
	displayOrder="15"
	category="CosmosDB Backup and Restore"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Point-in-time restore
Most users are able to resolve their queries related to point-in-time restore using the following steps.

## **Recommended Steps**

### **How can I enable point-in-time restore on existing accounts?**
This is not supported during preview

<br>

### **Feb 2021 public preview limitations**
Currently, the point-in-time restore functionality is in public preview and has the following limitations:
- Only Azure Cosmos DB APIs for SQL and MongoDB are supported for continuous backup. Cassandra, Table, and Gremlin APIs are not yet supported.
- An existing account with default periodic backup policy cannot be converted to use continuous backup mode
- Azure sovereign and Azure Government cloud regions not yet supported
- Accounts with customer-managed keys are not supported to use continuous backup
- Multi-regions write accounts are not supported
- Accounts with Synapse Link enabled are not supported
- The restored account is created in the same region where your source account exists. You can't restore an account into a region where the source account did not previously exist.
- The restore window is only 30 days and cannot be changed
- The backups are not automatically geo-disaster resistant. You must explicitly add another region to have resiliency for the account and the backup.
- While a restore is in progress, do not modify or delete the Identity and Access Management (IAM) policies that grant the permissions for the account or change any VNET, firewall configuration
- Azure Cosmos DB API for SQL or MongoDB accounts that create a unique index after the container is created are not supported for continuous backup. Only containers that create unique index as a part of the initial container creation are supported. For MongoDB accounts, you create unique index using extension commands.
- The point-in-time restore functionality always restores to a new Azure Cosmos account. Restoring to an existing account is currently not supported. If you are interested in providing feedback about in-place restore, contact the Azure Cosmos DB team via your account representative or UserVoice.
- All the new APIs exposed for listing `RestorableDatabaseAccount`, `RestorableSqlDatabases`, `RestorableSqlContainer`, `RestorableMongodbDatabase`, and `RestorableMongodbCollection` are subject to changes while the feature is in preview.
- After restoring, it is possible that for certain collections, the consistent index may be rebuilding. You can check the status of the rebuild operation via the `IndexTransformationProgress` property.
- The restore process restores all the properties of a container, including its TTL configuration. As a result, it is possible that the data restored is deleted immediately if you configured it that way. In order to prevent this situation, the restore timestamp must be before the TTL properties were added into the container.

<br>

### **What is restored?**
In a steady state, all mutations performed on the source account (including databases, containers, and items) are backed up asynchronously within 100 seconds. If the backup media (that is Azure storage) is down or unavailable, the mutations are persisted locally until the media is available. Then, they are flushed out to prevent any loss in fidelity of operations which can be restored.

You can choose to restore any combination of provisioned throughput containers, shared throughput database, or the entire account. The restore action restores all data and its index properties into a new account. The restore process ensures that all the data restored in an account, database, or a container is guaranteed to be consistent up to the restore time specified. The duration of restore will depend on the amount of data that needs to be restored.

<br>

### **What is not restored?**
The following configurations are not restored after the point-in-time recovery:
- Firewall, VNET, private endpoint settings
- Consistency settings. By default, the account is restored with session consistency.  
- Regions
- Stored procedures, triggers, UDFs

  You can add these configurations to the restored account after the restore is completed
  
<br>

### **Can you switch off or disable the point-in-time restore backups?**
No, after it's enabled, the point-in-time restore feature cannot be disabled

<br>

### **What is the retention for point-in-time restore?**
A point-in-time restore enabled account retains backups for a period of 30 days

<br>

### **Can a point-in-time restore interval be changed?**
No, currently you can't change the point-in-time restore interval.

<br>

### **Can you configure to take a backup in Read regions?**
Yes, this happens automatically in continuous backup mode

<br>

## **Recommended Documents**  

[Frequently asked questions on the Azure Cosmos DB point-in-time restore feature](https://docs.microsoft.com/azure/cosmos-db/continuous-backup-restore-frequently-asked-questions)
<br>This article lists frequently asked questions about the Azure Cosmos DB point-in-time restore functionality that is achieved by using the continuous backup mode.  

[Continuous backup with point-in-time restore feature in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/continuous-backup-restore-introduction)
<br>This article provides information for Azure Cosmos DBs point-in-time restore functionality.   

[Resource model for the Azure Cosmos DB point-in-time restore feature](https://docs.microsoft.com/azure/cosmos-db/continuous-backup-restore-resource-model)
<br>This article explains the resource model for the Azure Cosmos DB point-in-time restore feature. It explains the parameters that support the continuous backup and resources that can be restored in Azure Cosmos DB API for SQL and MongoDB accounts.  

[Online backup and on-demand data restore in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/online-backup-and-restore)
<br>Azure Cosmos DB automatically takes backups of your data at regular intervals. The automatic backups are taken without affecting the performance or availability of the database operations. All the backups are stored separately in a storage service. The automatic backups are helpful in scenarios when you accidentally delete or update your Azure Cosmos account, database, or container and later require the data recovery.    






