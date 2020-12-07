<properties
	pageTitle="Security in Azure Cosmos DB Managed Identities"
	description="Security in Azure Cosmos DB Managed Identities"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32783450"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-security-managed-identities"
	displayOrder="171"
	category="Security"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Cosmos DB Managed Identities (Public Preview)
Most users are able to resolve their Azure Cosmos DB Managed Identities (Public Preview) issue by using the following steps.

## **Recommended Steps**  

### **Only system-assigned managed identities are currently supported**
User-assigned managed identities will be supported in the near future.

### **Currently, system-assigned managed identities can only be used with customer-managed keys**
After a system-assigned identity has been created on your account, it can be used to configure the access policy of the Azure Key Vault instance hosting your encryption keys.

### **You cannot disable a system-assigned managed identity if it is being used**
Make sure that the identity is not used in the access policy of any Azure Key Vault instance before trying to disable it.

## **Recommended Documents**

[Azure Cosmos DB database security](https://docs.microsoft.com/azure/cosmos-db/database-security)
