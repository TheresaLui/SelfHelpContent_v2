<properties
	pageTitle="CosmosDB Backup and Restore" 
	description="Troubleshoot CosmosDB Backup and Restore related issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	ms.author="balaks"
	selfHelpType="resource"
	supportTopicIds="32636805, 32636825"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-admin-backuprestore"
	displayOrder="1"
	category="CosmosDB Backup and Restore"
/>

# Backup and restore
Most users are able to resolve their Backup and Restore case using the steps below.

## **Recommended Steps**

### **Data backup retention**
<br>Azure Cosmos DB automatically takes a backup of your database every 4 hours and at any point of time, only the latest 2 backups are stored. However, if the container or database is deleted, Azure Cosmos DB retains the existing snapshots of a given container or database for 30 days.
<br>We do have the option to increase the backups retention duration to help you customize.
<br>There are some limits for the backups:
* We can’t have any backup for more than 30 days
* The number of backups can’t be more than 25 at the same time
* The minimum backup interval is 1 hour

 
### **Performaing a restore**
<br>Microsoft can only do a copy of a Cosmos DB account within the same subscription and resource group. It is not possible to restore the database to a new subscription. 
The restore process always creates a new Azure Cosmos account to hold the restored data. The name of the new account, if not specified, will have the format <Azure_Cosmos_account_original_name>-restored1. The last digit is incremented, if multiple restores are attempted. You can’t restore data to a pre-created Azure Cosmos account.  


### **How long takes the restore**
There is no SLA for the Restore timelines.  But the Restore process can be broken down in to the following:
* The time to engage the Cosmos DB engineering team to initiate the restore based on the case severity.   
* The execution for the data restore depends upon the size of the data.  
 
Typical Guidelines 
* Minimum Restore Time approx. 10 Minutes
* 1 TB approx. 4 Hours or more  
**Note**:  NO SLA guarantee. The above times are an estimate.
 

### **Managing your own backups**
<br>We have 3 suggestions for you to clone your Cosmos DB to another Resource Group or even to the same to manage your own backups:
* You can use data [Cosmos DB Data Migration tool](https://azure.microsoft.com/updates/documentdb-data-migration-tool/), with the Azure Cosmos DB Data Migration tool you can easily migrate data to Azure Cosmos DB. The Azure Cosmos DB Data Migration tool is an open source solution.
* You can use Azure Data Factory (ADF), using ADF you can copy data from Azure Cosmos DB (SQL API) to another Azure Cosmos DB (SQL API)
* You can also use the [CosmicCLone tool](https://github.com/Microsoft/CosmicClone) where you can take a clone/backup with data/stored procedures/triggers/udf, etc.  

### **Reducing need for backups**
<br>Your Cosmos DB account may not require backup/restore for disaster recovery. Azure Cosmos DB provides [High availability with Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/high-availability) to transparently replicate your data across all the Azure regions associated with your Cosmos account

 

## **Recommended Documents**  

[Azure Cosmos DB backup and restore process and policy](https://docs.microsoft.com/azure/cosmos-db/online-backup-and-restore)
<br>This article describes how Azure Cosmos DB performs data backup.  

[multi-region accounts](https://docs.microsoft.com/azure/cosmos-db/how-to-manage-database-account)
<br>This article describes how to manage various tasks on an Azure Cosmos account using the Azure portal, Azure PowerShell, Azure CLI, and Azure Resource Manager templates.  

[Distribute data globally](https://docs.microsoft.com/azure/cosmos-db/distribute-data-globally)
<br>This article describes the Key benefits of global distribution
* Build global active-active apps
* Highly responsive apps
* Highly available apps
* Maintain business continuity during regional outages
* Scale read and write throughput globally
* Choose from several well-defined consistency models