<properties
	  pageTitle="MongoDB wire version issues"
	  description="MongoDB wire version issues"
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
	  articleId="0e79cf7a-a862-4659-b44b-8aa40c90b4eb"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# MongoDB wire version issues

<!--issueDescription-->

Dear customer,

The older versions of MongoDB drivers are unable to detect the Azure Cosmos account name in the connection strings.
- Append *appName=@accountName@* at the end of your Cosmos DBs API for MongoDB connection string, where *accountName* is your Cosmos DB account name.

Thank you.

<!--/issueDescription-->

