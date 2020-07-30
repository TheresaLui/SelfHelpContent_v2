<properties
    pageTitle="Key vault issues RCA"
    description="RCA - Cosmos DB account blocked by key vault"
    infoBubbleText="The Cosmos DB account is unable to contact the key vault. See the details on the right."
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="pratnala"
    ms.author="pratnala"
    articleId="cosmosdb-keyvaultwrap-rca"
    diagnosticScenario="CosmosDBKeyVaultWrapInsight"
    selfHelpType="rca"
    supportTopicIds="32636769, 32636770, 32636771, 32741326"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Issues with your linked key vault

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
The Cosmos DB account, **<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->** is unable to access the Azure Key Vault instance hosting your encryption key.
<!--/issueDescription-->

## **Recommended Steps**

It appears that your key vault's configuration is preventing your Cosmos DB account from contacting the key vault to access your managed encryption keys. If you've recently performed a key rotation, make sure that the previous key or key version remains enabled and available until Cosmos DB has completed the rotation. The previous key or key version can be disabled after 24 hours, or after the Azure Key Vault audit logs don't show activity from Azure Cosmos DB on that key or key version anymore.

## **Recommended Documents**

* [Setup customer-managed keys](https://docs.microsoft.com/azure/cosmos-db/how-to-setup-cmk)
