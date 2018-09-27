<properties
pageTitle="Azure Cosmos DB internal server error"
description="Internal server Error"
service="microsoft.documentdb"
resource="databaseAccounts"
authors="balaksms"
displayOrder="87"
selfHelpType="resource"
supportTopicIds="32597529"
resourceTags=""
productPesIds="15585"
cloudEnvironments="public"/>

# I am getting an internal server error when changing the scale setting in Azure Portal

## **Recommended Steps**

You can use Azure Portal or C# console application to modify the scale setting following the example below

### Change scale setting using Azure Portal

1. Browse to Azure Portal 
2. Suffix the Tag “?feature.enableSettingsBlade=true” at the end of the URL and hit enter
3. Browse to the Azure Cosmos database account and choose scale blade
4. Update the throughput value and save

### Change scale setting using C# console application

* [Change the scale setting using this sample code](https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.documentclient.replaceofferasync?view=azure-dotnet) to change the scale setting.

# I am getting an internal server error when using Azure Cosmos DB data explorer

## **Recommended Steps**

The data explorer uses the respective SDK i.e. SQL API or Mongo API to access the data from the Azure Cosmos DB.  Using a Azure Cosmos DB - SQL API SDK to perform CRUD operation against Mongo API account 
would not generate any error.  However, this would make the data explorer to fail when reading the data due to structure mismatch.

Please use the Azure Cosmos DB - Mongo API to perform CRUD operation against Azure Cosmos DB  - Mongo API account.


## **Recommended documents**

* [Retiring the S1, S2, and S3 performance levels]( https://docs.microsoft.com/azure/cosmos-db/performance-levels)
* [Set and get throughput for Azure Cosmos DB containers and database]( https://docs.microsoft.com/azure/cosmos-db/set-throughput)
* [How to get started](https://docs.microsoft.com/azure/cosmos-db/mongodb-introduction#how-to-get-started)
