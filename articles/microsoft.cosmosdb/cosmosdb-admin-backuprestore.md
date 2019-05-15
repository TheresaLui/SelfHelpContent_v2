<properties
	pageTitle="CosmosDB Backup and Restore" 
	description="CosmosDB Backup and Restore"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	ms.author="balaks"
	selfHelpType="generic"
	supportTopicIds="32636805, 32636825"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-admin-backuprestore"
/>

# Requesting backups to test disaster recovery

Azure Cosmos DB automatically backs up your data to guard against regional failures or accidental deletion. If you're requesting a backup to test disaster recovery, please enable a second geo-replicated region which would provide the option for manual or automatic failover. For more details, please refer to this article: [Distribute data globally](https://docs.microsoft.com/azure/cosmos-db/distribute-data-globally).

## **Recommended Steps**

Please continue to file a support ticket if you need help to restore an accidentally deleted account, database, collection, or document.

## **Recommended Documents**

* [Azure Cosmos DB backup process](https://docs.microsoft.com/azure/cosmos-db/online-backup-and-restore#high-availability-with-cosmos-db---a-recap)
* [Distribute data globally](https://docs.microsoft.com/azure/cosmos-db/distribute-data-globally)
