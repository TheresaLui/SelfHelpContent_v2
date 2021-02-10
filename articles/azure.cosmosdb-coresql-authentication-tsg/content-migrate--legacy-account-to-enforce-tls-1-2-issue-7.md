<properties
	  pageTitle="Migrate  legacy account to enforce TLS 1.2 issue"
	  description="Migrate  legacy account to enforce TLS 1.2 issue"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="21630207-7bd7-4958-a578-53370f6457b3"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Migrate  legacy account to enforce TLS 1.2 issue

Cosmos DB support TLS 1.2.  TLS 1.2 enforcement is based on the below factors

1. The account should be enabled to only allow TLS 1.2 connection
2. The Client SDK Version.  

The enforcement plan is as follows.

1. All **new account created on or after 29th July 2020** would be **enforcing the connection** to be TLS 1.2.
2. All legacy database account  to which a client is using TLS 1.2 would be migrated to enforce the TLS 1.2 seamlessly.  This means any connection using TLS version lower than 1.2 will be rejected after the migration and the client would get a clear error message.
3. Any legacy database account to which the client are **not using TLS 1.2** **would continue to work fine and no enforcement would be applied**.

Please point customer to the [Blog](https://devblogs.microsoft.com/cosmosdb/tls-1-2-enforcement/)

[Update 2020-10-29] New accounts may not be enforcing TLS 1.2. This is currently being deployed across our federations and not completed yet.  **Current ETA for new accounts to enforce TLS 1.2 is end of November 2020**.

