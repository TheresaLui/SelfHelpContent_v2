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
    supportTopicIds="32741326"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# IP Blocked by Firewall

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
The Cosmos DB account, **<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->** is having issues reaching the key vaults to access your encryption keys.
<!--/issueDescription-->

## **Recommended Steps**

It appears that your key vault's access control policies are preventing your Cosmos DB account from contacting the key vault to access your managed encryption keys.

## **Recommended Documents**

* [Setup customer-managed keys](https://docs.microsoft.com/azure/cosmos-db/how-to-setup-cmk)
