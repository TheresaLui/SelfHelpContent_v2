<properties
	pageTitle="Azure Cosmos DB Managed Keys"
	description="Azure Cosmos DB Managed Keys"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32741326"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-security-managedkeys"
	displayOrder="164"
	category="Security"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Azure Cosmos DB Managed Keys

Most users are able to resolve their Azure Cosmos DB Managed Keys issue using the steps below.


## **Recommended Steps**  

**Issue: You cannot create a CMK (Customer Managed Key) account and have verified all conditions are met**
The most common cause of account creation issues are inclusion of the version of the key in the create call 
example: /keys/p3rfrotatekey1/56b75982a81d471990af8f12be0933d4  

No version is permitted during provisioning  

In the AKV key the version is at the end and in this example is 56b75982a81d471880af8f12be0933d4. Once the version is removed (example: ../keys/p3rfrotatekey1 ) the creation will succeed. The reason Azure Cosmos DB does not accept a version is it automatically picks up the latest key within one hour of creation. This is called automatic rotation.  


**Issue: Azure Key Vault Key is revoked and you cannot create or delete a collection or database**
The only allowed operation when account keys are revoked is to delete the account. No other operations are permitted. You should restore key access and operation will be permitted once the account is fully operational which may take upto 1 hour.  


**Issue: You have restored key access but the account is still not operational**
Account revocation and access is throttled to once per hour. If you revoke a key, the account access is pulled, and then for restores, the key can take up to one hour to restore access to data. This is by design to prevent threshing of account resources and to protect you from accidental access issues.  


## **Recommended Documents**

[How to setup Customer Managed Keys](https://docs.microsoft.com/azure/cosmos-db/how-to-setup-cmk)
<br>Configure customer-managed keys for your Azure Cosmos account with Azure Key Vault  

