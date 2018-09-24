<properties
	pageTitle="CosmosDB Backup and Restore" 
	description="CosmosDB Backup and Restore"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	displayOrder="75"
	selfHelpType="resource"
	supportTopicIds="32597495"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
/>

# Requesting backups to test disaster recovery

Azure Cosmos DB automatically backs up your data to guard against regional failures or accidental deletion. If you're requesting a backup to test disaster recovery, please enable a second geo-replicated region which would provide the option for manual or automatic failover. Please review [Distribute data globally](https://docs.microsoft.com/azure/cosmos-db/distribute-data-globally) document.

Please continue to file a support ticket if you need help to restore an accidentally deleted account, database, collection or document.

## **Recommended documents**

* [Azure Cosmos DB backup process](https://docs.microsoft.com/azure/cosmos-db/online-backup-and-restore#high-availability-with-cosmos-db---a-recap)
* [Distribute data globally](https://docs.microsoft.com/azure/cosmos-db/distribute-data-globally)
