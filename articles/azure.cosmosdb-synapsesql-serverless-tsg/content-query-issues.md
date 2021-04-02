<properties
 pageTitle="TLDC1 Query Issues"
 description="TLDC1 Query Issues"
 service="Microsoft.DocumentDB"
 resource="Microsoft.DocumentDB/databaseAccounts"
 authors="AzureData_AzureCosmosDB"
 ms.author="AzureData_AzureCosmosDB"
 displayOrder=""
 selfHelpType="TSG_Content"
 supportTopicIds=""
 resourceTags=""
 productPesIds=""
 cloudEnvironments="public, fairfax, usnat, ussec"
 articleId="34b458a0-89eb-41fe-8cf1-8acd7c91f620"
 ownershipId="AzureData_AzureCosmosDB"
/>

# TLDC1 Query Issues

### Common Query Issues

<br>
<br>


#### My query isn't showing the data I just inserted into Azure Cosmos DB Container
Azure Cosmos DB will sync your transactional data with analytical store within 2 and 5 minutes. Please wait up to 5 minutes and re-run your query.  

<br>

#### My query isn't working with the Linked Service for Azure Cosmos DB that I created
Support for Linked Services is planned for the first semester of 2021. For now you need to use OPENROWSET function. When available, it will work for Linked Services for Azure Cosmos DB containers with analytical store enabled.  

<br>

#### Can't load data into Cosmos DB using SQL Serverless
Synapse SQL Serverless is read only.   

<br>

#### My query isn't returning some documents
If you are using SQL API, it is "well defined schema" by default, meaning that the first document in the collection will defined the analytical store schema. Documents that violate that format won't be synced to analytical store.

<br>
<br>