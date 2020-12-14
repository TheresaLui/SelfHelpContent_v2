<properties
	  pageTitle="Predicate included in Index path"
	  description="Predicate included in Index path"
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
	  articleId="4a83a4e0-803e-4453-ab7b-c6361447d4cf"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Predicate included in Index path

The complexity of a query affects how many Request Units are consumed for an operation. The number of predicates, the nature of the predicates, and the size of the source dataset all influence the cost of query operations.

1. Get the customer query
2. Check if the fields being used are indexed

