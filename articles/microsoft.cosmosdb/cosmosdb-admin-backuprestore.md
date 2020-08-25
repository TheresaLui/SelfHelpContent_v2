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

### **Changing backup interval and retention period**
Azure Cosmos DB automatically takes a backup of your data for every 4 hours and at any point of time, the latest two backups are stored. This configuration is the default option and it is offered without any additional cost. You can change these default backup interval and retention period during the Azure Cosmos account creation or after the account is created. The backup configuration is set at the Azure Cosmos account level and you need to configure it on each account. After you configure the backup options for an account, it is applied to all the containers within that account. Currently you can change them backup options from Azure portal only.  

If the number of copies end up more than 2, you will be charged for those additional copies. See the Consumed Storage section in the [Pricing page](https://azure.microsoft.com/pricing/details/cosmos-db/) to know the exact price for additional copies.

If you would like to change the default backup options for an existing Azure Cosmos account, please see the link [Backup interval and retention period](https://docs.microsoft.com/azure/cosmos-db/online-backup-and-restore#backup-interval-and-retention-period) to change your backup retention using Azure Portal.   

![Backup Retention visual](https://docs.microsoft.com/azure/cosmos-db/media/online-backup-and-restore/configure-backup-interval-retention.png)  

<br>

### **Requesting a restore**
If you have accidentally deleted or corrupted your data, **before you create a support request to restore the data, make sure to increase the backup retention for your account to at least seven days. It is best to increase your retention within 8 hours of this event.** This way, the Azure Cosmos DB team has enough time to restore your account.

The restore process always creates a new Azure Cosmos account to hold the restored data. The name of the new account, if not specified, will have the format <Azure_Cosmos_account_original_name>-restored1. The last digit is incremented if multiple restores are attempted. You cannot restore data to a pre-created Azure Cosmos account.  

Microsoft can only do a copy of a Cosmos DB account within the same subscription and resource group. It is not possible to restore the database to a new subscription. If you need a copy of your data in a new subscription, please use the [Cosmos DB Data Migration tool](https://azure.microsoft.com/updates/documentdb-data-migration-tool/).  





### **How long a restore takes**
There is no SLA for restore timelines.
<br>However, the restore process can be broken down into the following:
* The time to engage the Cosmos DB engineering team to initiate the restore based on the case severity
* The execution for the data restore depends upon the size of the data. As an example, once a restore has been initiated for 500 GB of data the approximate restore time could be about 4 hours.
**Note**:  There is no SLA guarantee. The above times are an estimate.  

 

### **Managing your own backups**
We have some suggestions for how you can clone your Cosmos DB to another Resource Group or even to the same RG to manage your own backups:
* You can use the [Cosmos DB Data Migration tool](https://azure.microsoft.com/updates/documentdb-data-migration-tool/). With the Azure Cosmos DB Data Migration tool you can easily migrate data to Azure Cosmos DB. The Azure Cosmos DB Data Migration tool is an open source solution.
* You can use Azure Data Factory (ADF), using ADF you can copy data from Azure Cosmos DB (SQL API) to another Azure Cosmos DB (SQL API)  



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