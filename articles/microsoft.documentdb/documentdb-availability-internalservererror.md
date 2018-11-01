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

# Getting internal server error

## I am getting an internal server error when changing the Scale setting in Azure Portal

## **Recommended Steps**

You can use the Azure Portal or C# console application to modify the scale setting using following the steps:

### 1. Change the Scale setting using Azure Portal

1. Browse to [Azure Portal](https://ms.portal.azure.com) 
2. Add “?feature.enableSettingsBlade=true” at the end of the URL and click enter
3. Browse to the Azure Cosmos DB account and choose Scale blade
4. Update the throughput value and save

### 2. Change the Scale setting using a C# console application

[Change the scale setting using this sample code](https://github.com/Azure/azure-documentdb-dotnet/blob/95521ff51ade486bb899d6913880995beaff58ce/samples/code-samples/CollectionManagement/Program.cs#L198)

## I am getting an internal server error when using Azure Cosmos DB Data Explorer

The Data Explorer uses the SDK that corresponds to each Azure Cosmos DB API account to access the data from the Azure Cosmos DB. Using the Azure Cosmos DB SQL API SDK to perform CRUD operations against MongoDB API account would not generate any error. However, this would make the Data Explorer produce an internal server error when reading the data due to a mismatch in the data formats.

## **Recommended Steps**

Delete the documents created through SQL API from the Mongo Collection using Document Studio. Using MongoDB SDK to perform CRUD operations against Azure Cosmos DB MongoDB API account would help you to resolve this issue. 

Please open a support ticket including the activity ID and timestamp of the request if your scenario for internal server error does not match with any of the cases mentioned above.

## **Recommended documents**

* [Retiring the S1, S2, and S3 performance levels]( https://docs.microsoft.com/azure/cosmos-db/performance-levels)
* [Set and get throughput for Azure Cosmos DB containers and database]( https://docs.microsoft.com/azure/cosmos-db/set-throughput)
* [Get started with Azure Cosmos DB Mongo API](https://docs.microsoft.com/azure/cosmos-db/mongodb-introduction#how-to-get-started)
