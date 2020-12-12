<properties
	pageTitle="Azure Cosmos DB - General Advisory"
	description="Azure Cosmos DB - General Advisory"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32741541"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-advisory-other"
	displayOrder="40"
	category="General Advisory"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Cosmos DB - General Advisory

Most users are able to resolve their General Advisory Questions using the steps below.

## **Recommended Steps**

### **Unable to register for Preview Features**

Issue: I want to preview some new features but I am not able to complete the registration in the portal.

- The account may be missing the required permission
- The subscription also would require Resource Provider "Microsoft.Features" to be registered

For additional information please see [Microsoft.Features](https://docs.microsoft.com/azure/role-based-access-control/resource-provider-operations#microsoftfeatures).

### **Data backup retention**

Azure Cosmos DB automatically takes a backup of your database every 4 hours and at any point of time, only the latest 2 backups are stored. However, if the container or database is deleted, Azure Cosmos DB retains the existing snapshots of a given container or database for 30 days.

<br>We do have the option to increase the backups retention duration to help you customize.  

There are some limits for the backups:

* Backups cannot be retained for more than 30 days
* The number of backups cannot be more than 25 at the same time
* The minimum backup interval is 1 hour  

## **Recommended Documents**

[How to model and partition in Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/how-to-model-partition-example)
<br>This article builds on several Azure Cosmos DB concepts like data modeling, partitioning, and provisioned throughput to demonstrate how to tackle a real-world data design exercise.  

[Cosmos DB Limits](https://docs.microsoft.com/azure/cosmos-db/concepts-limits)
<br>This article provides an overview of the default quotas offered to different resources in the Azure Cosmos DB.  

[Cosmos DB FAQs](https://docs.microsoft.com/azure/cosmos-db/faq)
<br>Frequently asked questions about different APIs in Azure Cosmos DB.  

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
