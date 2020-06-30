<properties
    pageTitle="Upgrade your Azure Cosmos DB Java SDK to the latest version from Maven"
    description="Upgrade your Azure Cosmos DB Java SDK to the latest version from Maven"
    authors="pratnala"
    ms.author="pratnala"
    articleId="3312d528-e60e-4d3a-8dd0-e97f030c4681_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Upgrade your Azure Cosmos DB Java SDK to the latest version from Maven
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "3312d528-e60e-4d3a-8dd0-e97f030c4681",
  "dataSourceMetadata": {
    "dataSource": "Kusto",
      "streamNamespace": "cluster('https://cdbsupport.kusto.windows.net').database('Support').OldJavaSDK",
      "refreshInterval": "0.12:00:00",
    "schemaVersion": 3.0
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDbUpgradeJavaSdk",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "cosmosnotifications@microsoft.com",
    "icm": {
      "routingId": "mdm://adspartner/CosmosDB",
      "service": "Azure Cosmos DB",
      "team": "Supportability"
    },
    "serviceTreeId": "724c33bf-1ab8-4691-adb1-0e61932919c2"
  },
  "version": 2.6,
  "learnMoreLink": "https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-java-v4",
  "description": "Upgrade your Azure Cosmos DB Java SDK to the latest version from Maven",
  "longDescription": "Your Azure Cosmos DB account is using an old version of the Java SDK. We recommend upgrading to the latest version from Maven for latest fixes, performance improvements, and new feature capabilities.",
  "potentialBenefits": "Improved reliability, performance, and new feature capabilities",
  "displayLabel": "Upgrade your Azure Cosmos DB Java SDK to the latest version from Maven",
  "additionalColumns": [
    {
      "name": "RecommendedVersion",
      "title": "Minimum Recommended Version"
    },
    {
      "name": "CurrentVersion",
      "title": "Current Version"
    }
  ],
  "actions": [
    {
      "actionId": "68e6f866-956c-4fd9-b16a-916222b663b6",
      "description": "Upgrade your Java SDK",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-java-v4"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "7b999253-6a98-4f48-96c1-2852be4db70c",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_DocumentDB",
      "bladeName": "DatabaseAccountTemplateBladeForGlobalDb",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  }
}
---
