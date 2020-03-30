<properties
	pageTitle="Manage an Azure Cosmos account"
	description="Troubleshoot CosmosDB Account provisioning or management related issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="markjbrown"
	ms.author="mjbrown"
	selfHelpType="generic"
	supportTopicIds="32636765, 32681011"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake"
	articleId="cosmosdb-admin-account-management"
	displayOrder="20"
	category="Administration"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Manage an Azure Cosmos account
Most users are able to resolve their Account provisioning or management issue using the steps below.

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


### **Not able to delete a resource group**  
If you are not able to delete a resource group, please consider the following solutions:  
* Verify if there is a *lock* on an account located in the resource group that is preventing it from being deleted. You can verify this by navigating to the *Account* blade, selecting the account, and then view *Locks*.
* Verify if you have a *delete lock* enabled on your resource group. You can verify this by navigating to the *Resource Group* blade, select the resource where the account is located, and then view *Locks*.
* You also may have a lock on an additional items located within the resource group.  It is recommended to review the items for any enabled *Delete Locks*.  

### **Unable to update Consistency as well as disable multi-region writes**
With VNET enabled accounts, the selected user making changes to the account must have permissions on the VNET.
* Add the necessary permissions to the desired user to make changes or assign another user with the expected permissions to update the consistency 

## **Recommended Documents**  

The below recommended documents describes how to manage various tasks on an Azure Cosmos account using the Azure portal, Azure PowerShell, Azure CLI, and Azure Resource Manager templates.

[Managing Azure Cosmos Account](https://docs.microsoft.com/azure/cosmos-db/how-to-manage-database-account)
<br>This article describes how to manage various tasks on an Azure Cosmos account using the Azure portal:
* Create an account
* Add/remove regions from your database account
* Configure multiple write-regions
* Enable automatic failover for your Azure Cosmos account
* Set failover priorities for your Azure Cosmos account
* Perform manual failover on an Azure Cosmos account  


[Azure Resource Manager templates for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/resource-manager-samples)
<br>This article includes links to Azure Resource Manager templates for Azure Cosmos DB:
* SQL (Core) API
* MongoDB API
* Cassandra API
* Gremlin API
* Table API  

[Azure CLI samples for Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/cli-samples)
<br>This article includes links to sample Azure CLI scripts for Azure Cosmos DB SQL (Core) API.  

[PowerShell samples for Azure Cosmos DB SQL (Core) API](https://docs.microsoft.com/azure/cosmos-db/powershell-samples-sql)
<br>This article includes samples to commonly used Azure PowerShell scripts for Azure Cosmos DB for SQL (Core) API.  

[Azure Lock Management](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources)
<br>As an administrator, you may need to lock a subscription, resource group, or resource to prevent other users in your organization from accidentally deleting or modifying critical resources. This article covers how to enable locks in the Portal and the intent for each lock type.