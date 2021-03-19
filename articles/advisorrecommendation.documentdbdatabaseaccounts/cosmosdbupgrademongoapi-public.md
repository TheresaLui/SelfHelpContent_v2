<properties
    pageTitle="Upgrade your Azure Cosmos DB's API for MongoDB to version 3.6"
    description="Upgrade your Azure Cosmos DB's API for MongoDB to version 3.6"
    authors="pratnala"
    ms.author="pratnala"
    articleId="0da795d9-26d2-4f02-a019-0ec383363c88_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, USNat, USSec"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Upgrade your Azure Cosmos DB's API for MongoDB to version 3.6
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "0da795d9-26d2-4f02-a019-0ec383363c88",
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DocumentDb/databaseAccounts",
  "recommendationFriendlyName": "CosmosDBUpgradeMongoAPI",
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
  "version": 0.2,
  "learnMoreLink": "https://docs.microsoft.com/azure/cosmos-db/mongodb-feature-support-36",
  "description": "Upgrade your Azure Cosmos DB's API for MongoDB to version 3.6",
  "longDescription": "Your Azure Cosmos DB account qualifies to be upgraded to version 3.6 of Azure Cosmos DB's API for MongoDB. We recommend upgrading to version 3.6 for the most up-to-date functionality, the latest fixes, and enhancements in performance and stability.",
  "potentialBenefits": "Improved reliability, performance, and new feature capabilities",
  "displayLabel": "Upgrade your Azure Cosmos DB's API for MongoDB to version 3.6",
  "dataSourceMetadata": {
    "dataSource": "Kusto",
    "streamNamespace": "cluster('https://cdbsupport.kusto.windows.net').database('Support').MongoAdvisor",
    "refreshInterval": "0.12:00:00"
  },
  "actions":[
    {
      "actionId": "e2480b31-2e55-476f-ab85-13b42b4646f7",
      "description": "Upgrade to version 3.6",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_DocumentDB",
      "bladeName": "FeaturesBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "6aa03a6c-4ee6-45e3-9a04-9273449a6ea9",
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
