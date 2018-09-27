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

To resolve this issue, try one or more of the following methods

* Browse to Azure Portal 
* Suffix the Tag “?feature.enableSettingsBlade=true” at the end of the URL and hit enter
* Change the Scale Setting as needed.

Or

* [Change the scale setting using this sample code](https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.documentclient.replaceofferasync?view=azure-dotnet) to change the scale setting.


## **Recommended documents**

* [Retiring the S1, S2, and S3 performance levels]( https://docs.microsoft.com/azure/cosmos-db/performance-levels)
* [Set and get throughput for Azure Cosmos DB containers and database]( https://docs.microsoft.com/azure/cosmos-db/set-throughput)
