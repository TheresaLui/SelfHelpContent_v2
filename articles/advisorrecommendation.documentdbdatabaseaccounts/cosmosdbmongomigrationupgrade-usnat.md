<properties
    pagetitle="Migrate your Azure Cosmos DB's API for MongoDB account to version 3.6"
    description="Migrate your Azure Cosmos DB's API for MongoDB account to version 3.6"
    authors="pratnala"
    ms.author="pratnala"
    articleId="ceb9372d-60f6-4564-8033-a8b1ead4fa76_USNat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USNat"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Migrate your Azure Cosmos DB's API for MongoDB account to version 3.6
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "ceb9372d-60f6-4564-8033-a8b1ead4fa76",
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDBMongoMigrationUpgrade",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "cosmosnotifications@microsoft.com",
    "icm": {
      "routingId": "mdm://adspartner/CosmosDb",
      "service": "Azure Cosmos DB",
      "team": "Supportability"
    },
    "serviceTreeId": "724c33bf-1ab8-4691-adb1-0e61932919c2"
  },
  "version": 1.1,
  "learnMoreLink": "https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36",
  "description": "Migrate your Azure Cosmos DB's API for MongoDB account to version 3.6",
  "longDescription": "Migrate your database account to a new database account to take advantage of Azure Cosmos DB's API for MongoDB v3.6. This version provides the most up-to-date functionality, as well as enhancements in performance and stability. When upgrading the service, you must also migrate the data in your existing account to a new account created using version 3.6 of the MongoDB API engine. Azure Data Factory or Studio 3T can assist you in migrating your data.",
  "potentialBenefits": "Improved reliability, performance, and new feature capabilities",
  "displayLabel": "Migrate your Azure Cosmos DB's API for MongoDB account to version 3.6",
  "dataSourceMetadata": {
    "dataSource": "Kusto",
    "streamNamespace": "cluster('https://cdbusnateast.usnateast.kusto.core.eaglex.ic.gov').database('Support').MongoMigrationUpgradeAdvisor",
    "refreshInterval": "0.12:00:00"
  },
  "actions": [
    {
      "actionId": "39561308-0991-4188-8635-130d3c1ba91e",
      "description": "Migrate your data with Azure Data Factory",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/data-factory/connector-azure-cosmos-db-mongodb-api"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "9ccdcd86-d178-4248-a7e5-f63dfe6f6698",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_DocumentDB",
      "bladeName": "MongoAccountTemplateBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  }
}
---
