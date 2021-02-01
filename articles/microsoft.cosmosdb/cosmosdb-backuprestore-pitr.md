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
	displayOrder="14"
	category="CosmosDB Backup and Restore"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Backup and restore
Most users are able to resolve their Enable Point in Time Restore issue using the steps below.

## **Recommended Steps**

### **How to enable PITR on Existing accounts?**
- This is currently not supported during preview

### **What is not supported in Jan 2021 preview**
- Cassandra, Table, Gremlin not supported
- Gov/National regions not supported
- BYOK/CMK accounts not supported
- Multiwrite enabled accounts not supported
- The point-in-time restore process always restores to a new account
- Existing account can not be converted to use continuous backup
- No Toggling between continuous backup to periodic mode
- Dataplane RBAC enabled accounts are not supported
- SynapseLink – Accounts with Synapse link can not be opted in with Continuous Backup
- Cross region restores are not supported
- Inplace restore not supported
- The restore window is only 30 days. This cannot be changed.
- The backups are not automatically geo disaster resistant. Customers need to add another region to get resiliency for account as well as backup.
- While a restore is in progress, do not modify or delete the Identity and Access Management (IAM) policies that grant the permissions for the account or change any vnet/firewall.
  
### **What is restored?**
- Data
- Creation time Index for a collection
- Creation time TTL

### **What is not restored?**
- Latest RU setting or offer.  The account administrator can apply the required throughput.
- UDF/SPROC/Triggers.  The account administrator can add these as required.
- User/Permissions.  The account administrator can add these as required.
- Regions.  The account administrator can add these as required.
- VNET, Firewall settings can be added as required
- Consistency.  Default session consistency is restored, however this can be changed as required.
  
  
### **Can you switch off or disable the PITR backups?**
- No, once turned on, PITR cannot be disabled


### **What is the retention for PITR?**
- A PITR enabled account, retains backups for a period of 30 days

### **Can PITR interval be changed?**
- No

### **Can you configure to take a backup in Read regions?**
- Yes, this happens in continuous backup mode automatically

## **Recommended Documents**  

[Frequently asked questions on the Azure Cosmos DB point-in-time restore feature](https://docs.microsoft.com/azure/cosmos-db/continuous-backup-restore-frequently-asked-questions)
<br>This article lists frequently asked questions about the Azure Cosmos DB point-in-time restore functionality that is achieved by using the continuous backup mode.  

[Continuous backup with point-in-time restore feature in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/continuous-backup-restore-introduction)
<br>This article provides information for Azure Cosmos DBs point-in-time restore funtionality.   

[Resource model for the Azure Cosmos DB point-in-time restore feature](https://docs.microsoft.com/azure/cosmos-db/continuous-backup-restore-resource-model)
<br>This article explains the resource model for the Azure Cosmos DB point-in-time restore feature. It explains the parameters that support the continuous backup and resources that can be restored in Azure Cosmos DB API for SQL and MongoDB accounts.  

[Online backup and on-demand data restore in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/online-backup-and-restore)
<br>Azure Cosmos DB automatically takes backups of your data at regular intervals. The automatic backups are taken without affecting the performance or availability of the database operations. All the backups are stored separately in a storage service. The automatic backups are helpful in scenarios when you accidentally delete or update your Azure Cosmos account, database, or container and later require the data recovery.    






