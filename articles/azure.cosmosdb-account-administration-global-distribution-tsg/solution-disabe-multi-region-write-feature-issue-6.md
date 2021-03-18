<properties
	  pageTitle="Disabe Multi-region write feature issue"
	  description="Disabe Multi-region write feature issue"
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
	  articleId="ef6b92df-03d7-4367-a5ef-6f1b0a109da0"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Disabe Multi-region write feature issue

<!--issueDescription-->

Dear customer,

The Multi-region Write or Multi Master feature is an option which can be enabled during the Cosmos DB Account Creation work flow in the Azure Portal. 

##What is the default setting of Multi-region Write feature during Azure Cosmos DB Account Creation
The Multi-region Write feature is disabled by default in both the Portal and the Azure CLI. The setting option have to be enabled by the end user explicitly.

##How to Disable Azure Cosmos DB Multi-region Write feature from existing  Azure Cosmos DB Account?
The option to disable multi region write is available in the Azure Portal. Go to your Cosmos DB account > Replicate data globally > In the **Configure regions** select **Disable**.

You can also run the below azure CLI command to disable the Multi-region Write feature on an existing Cosmos DB Account, as an example:
```
az cosmosdb update  --name <database_name>  --resource-group <resource_group>  --enable-multiple-write-locations false 
```

**Note:** this should be executed in the Cloud Shell or if local, the latest version of Azure CLI.

# Recommended Documents:
[Public Documentation- Configure multiple write-regions](https://docs.microsoft.com/azure/cosmos-db/how-to-manage-database-account#configure-multiple-write-regions)   
[Public Documentation- Configure multi-master in your applications](https://docs.microsoft.com/azure/cosmos-db/how-to-multi-master)  

Thank you.

<!--/issueDescription-->

