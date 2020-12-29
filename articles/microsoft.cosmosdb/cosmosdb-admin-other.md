<properties
	pageTitle="Azure Cosmos DB Administration Other Topics"
	description="Troubleshoot other CosmosDB Administration related issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32741532"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-admin-other"
	displayOrder="28"
	category="Administration"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Cosmos DB Administration Other Topics

Most users are able to resolve their Administration case using the steps below.  

## **Recommended Steps**  

### **Not able to remove or add a region**

If you are not able to remove a region in your database account please consider the following solutions:  

* In a single-region write mode, you cannot remove the write region. You must fail over to a different region before you can delete the current write region. [Perform manual failover on an Azure Cosmos account](https://docs.microsoft.com/azure/cosmos-db/how-to-manage-database-account#manual-failover).
* In a multi-region write mode, you can add or remove any region, if you have at least one region.
* You cannot change another account property while adding or removing a region. To remedy, change the other account properties first, then retry the region change. You can compare property values by exporting the account to a template and compare currently property values from those set by your template, including tags.

### **Not able to delete an account**  

If after attempting to delete an account, you observe that nothing seems to happen and the account persists:

* Verify if you have a *delete lock* enabled on the account.  You can verify this by navigating to the *Account* blade, selecting the account, and then view *Locks*.
* Verify if you have a *delete lock* enabled on your resource group. You can verify this by navigating to the *Resource Group* blade, select the resource where the account is located, and then view *Locks*.
* See [Azure Lock Management](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources) for additional information

### **Unable to update Consistency as well as disable multi-region writes**

With VNET enabled accounts, the selected user making changes to the account must have permissions on the VNET.

* Add the necessary permissions to the desired user to make changes or assign another user with the expected permissions to update the consistency 

### **Azure Policy was not honored**

Policies that are created using Azure Policy only apply to changes made against the Cosmos DB resource provider. To ensure enforcement of Azure Policies, the account must be locked down to prevent changes by users accessing the account using any of the Cosmos DB SDKs. For more information on how to configure your account to ensure Azure Policy enforcement see, [Preventing changes from Azure Cosmos DB SDKs](https://docs.microsoft.com/azure/cosmos-db/role-based-access-control#prevent-sdk-changes)

## **Recommended Documents**

[Manage Azure Cosmos DB using PowerShell](https://docs.microsoft.com/azure/cosmos-db/manage-with-powershell)
<br>The following guide describes how to use PowerShell to script and automate management of Azure Cosmos DB resources, including account, database, container, and throughput. Management of Azure Cosmos DB is handled through the AzResource cmdlet directly to the Azure Cosmos DB resource provider.   

* [PowerShell samples for SQL (Core) API](https://docs.microsoft.com/azure/cosmos-db/powershell-samples-sql)
* [PowerShell samples for Cassandra API](https://docs.microsoft.com/azure/cosmos-db/powershell-samples-cassandra)
* [PowerShell samples for MongoDB API](https://docs.microsoft.com/azure/cosmos-db/powershell-samples-mongodb)
* [PowerShell samples for Gremlin API](https://docs.microsoft.com/azure/cosmos-db/powershell-samples-gremlin)
* [PowerShell samples for Table API](https://docs.microsoft.com/azure/cosmos-db/powershell-samples-table)  

[Manage Azure Cosmos using Azure CLI](https://docs.microsoft.com/azure/cosmos-db/manage-with-cli)
<br>The following guide describes common commands to automate management of your Azure Cosmos DB accounts, databases and containers using Azure CLI. Reference pages for all Azure Cosmos DB CLI commands are available in the Azure CLI Reference.  

[Manage Azure Cosmos DB using ARM Templates](https://docs.microsoft.com/azure/cosmos-db/manage-sql-with-resource-manager)
<br>In this article, you learn how to use Azure Resource Manager templates to help automate management of your Azure Cosmos DB accounts, databases, and containers.  

[FAQs](https://docs.microsoft.com/azure/cosmos-db/faq)
<br>Frequently asked questions about different APIs in Azure Cosmos DB.