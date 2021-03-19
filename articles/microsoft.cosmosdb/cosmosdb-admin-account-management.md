<properties
	pageTitle="Manage an Azure Cosmos account"
	description="Troubleshoot CosmosDB Account provisioning or management related issues"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="markjbrown"
	ms.author="mjbrown"
	selfHelpType="generic"
	supportTopicIds="32636765"
	resourceTags=""
	productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-admin-account-management"
	displayOrder="20"
	category="Administration"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Manage an Azure Cosmos account

Most users are able to resolve their Account provisioning or management issue using the steps below.

## **Recommended Steps**

### **Not able to remove or add a region**

If you are not able to remove a region in your database account, consider the following solutions:

* In a single-region write mode, you cannot remove the write region. You must fail over to a different region before you can delete the current write region. See [perform manual failover on an Azure Cosmos account](https://docs.microsoft.com/azure/cosmos-db/how-to-manage-database-account#manual-failover).
* In a multi-region write mode, you can add or remove any region, if you have at least one region
* You cannot change another account property while adding or removing a region. Instead, change the other account properties first, then retry the region change. You can compare property values by exporting the account to a template and compare currently property values from those set by your template, including tags.

### **Not able to delete an account**

If after trying to delete an account, nothing seems to happen and the account persists:

* Verify if you have a *delete lock* enabled on the account.  You can verify this by navigating to the *Account* blade, selecting the account, and then view *Locks*.
* Verify if you have a *delete lock* enabled on your resource group. You can verify this by navigating to the *Resource Group* blade, select the resource where the account is located, and then view *Locks*.  

### **Not able to delete a resource group**

If you are not able to delete a resource group, consider the following solutions:

* Verify if there is a *lock* on an account located in the resource group that is preventing it from being deleted. You can verify this by navigating to the *Account* blade, selecting the account, and then view *Locks*.
* Verify if you have a *delete lock* enabled on your resource group. You can verify this by navigating to the *Resource Group* blade, select the resource where the account is located, and then view *Locks*.
* You also may have a lock on an additional items located within the resource group. We recommend reviewing the items for any enabled *Delete Locks*.  

### **Unable to update Consistency as well as disable multi-region writes**

With VNet-enabled accounts, the user making changes to the account must have permissions on the VNet:

* Add the necessary permissions to the user to make changes or assign another user with the necessary permissions to update the consistency

### **Find out who made changes to an Azure Cosmos DB account**

If you need to find out who or when changes were made to your Cosmos DB account or get alerts when specific changes are made, you can enable this capability in Cosmos DB. Learn [how to audit Azure Cosmos DB control plane operations](https://docs.microsoft.com/azure/cosmos-db/audit-control-plane-logs).

### **Azure Policy was not honored**

Policies that are created using Azure Policy apply only to changes made against the Cosmos DB resource provider. To ensure enforcement of Azure Policies, the account must be locked down to prevent changes by users accessing the account using any of the Cosmos DB SDKs. For more information on how to configure your account to ensure Azure Policy enforcement, see [Preventing changes from Azure Cosmos DB SDKs](https://docs.microsoft.com/azure/cosmos-db/role-based-access-control#prevent-sdk-changes).

### **Cannot create account using customer managed key**

If you receive an error message of "Forbidden" that includes the phrase, "...does not have keys get permission on key vault," this is likely due to a missing access policy to your key vault instance. For instructions on how to add an access policy to your Azure Key Vault instance, see [configure customer-managed keys for your Azure Cosmos account with Azure Key Vault](https://docs.microsoft.com/azure/cosmos-db/how-to-setup-cmk#add-an-access-policy-to-your-azure-key-vault-instance).

## **Recommended Documents**  

The following recommended documents describe how to manage various tasks on an Azure Cosmos account using the Azure portal, Azure PowerShell, Azure CLI, and Azure Resource Manager templates.

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
<br>This article includes links to sample Azure CLI scripts for Azure Cosmos DB.  

[PowerShell samples for Azure Cosmos DB SQL (Core) API](https://docs.microsoft.com/azure/cosmos-db/powershell-samples)
<br>This article includes samples to commonly used Azure PowerShell scripts for Azure Cosmos DB.  

[Azure Lock Management](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources)
<br>As an administrator, you may need to lock a subscription, resource group, or resource to prevent other users in your organization from accidentally deleting or modifying critical resources. This article covers how to enable locks in the portal and the purpose for each lock type.
