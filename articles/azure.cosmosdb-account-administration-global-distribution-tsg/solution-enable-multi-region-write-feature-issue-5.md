<properties
	  pageTitle="Enable Multi-region write feature issue"
	  description="Enable Multi-region write feature issue"
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
	  articleId="0feaad8f-3da9-46cd-a87b-30cc583cfe0f"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Enable Multi-region write feature issue

<!--issueDescription-->

Dear customer,

The Multi-region Write or Multi Master feature is an option which can be enabled during the Cosmos DB Account Creation work flow in the Azure Portal. 

##What is the default setting of Multi-region Write feature during Azure Cosmos DB Account Creation
The Multi-region Write feature is disabled by default in both the Portal and the Azure CLI. The setting option have to be enabled by the end user.

##How to enable Azure Cosmos DB Multi-region Write feature on an existing Azure Cosmos DB Account?
The Azure Portal can be used to enable the multi-region write feature. Go to your Cosmos DB account > Replicate data globally > In the **Configure regions** select **Enable**.

You can also run the below azure CLI command to enable the Multi-region Write feature on an existing Cosmos DB Account, as an example:
**az cosmosdb update --name testdefaultmultisetting --resource-group CSSCASES --enable-multiple-write-locations True --id /subscriptions/092edcdf-b871-43c0-bc3f-434f835467df/resourceGroups/CSSCASES/providers/Microsoft.DocumentDB/databaseAccounts/sqldisablemr**
 
**Note:** this should be executed in the Cloud Shell or if local, in the latest version of Azure CLI.

# Recommended Documents:
[Public Documentation- Configure multiple write-regions](https://docs.microsoft.com/azure/cosmos-db/how-to-manage-database-account#configure-multiple-write-regions)   
[Public Documentation- Configure multi-master in your applications](https://docs.microsoft.com/azure/cosmos-db/how-to-multi-master)  

Thank you.

<!--/issueDescription-->

