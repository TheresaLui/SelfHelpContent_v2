<properties
	  pageTitle="How to get the name of a Cosmos DB Collection"
	  description="How to get the name of a Cosmos DB Collection"
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
	  articleId="b251f139-ff27-4051-9a75-fc04fb53b245"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# How to get the name of a Cosmos DB Collection

<!--issueDescription-->

Dear customer,

To get the name of a Cosmos DB Collection, use the Azure CLI Command from your machine. 
After installing the CLI execute the below:
- az login (to login to your account) and then you can List the Collections with all of their information, and check the ID for which Collection
- az cosmosdb collection list -d <DBname> -n <DatabaseAccountNAme> -g <ResourceGroupNAme>

Thank you.

<!--/issueDescription-->

