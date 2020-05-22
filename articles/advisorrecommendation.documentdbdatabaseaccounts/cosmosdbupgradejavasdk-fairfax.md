<properties
    pageTitle="Upgrade your Azure Cosmos DB Java SDK to the latest version from Maven"
    description="Upgrade your Azure Cosmos DB Java SDK to the latest version from Maven"
    authors="rnagpal"
    ms.author="rnagpal"
    articleId="3312d528-e60e-4d3a-8dd0-e97f030c4681_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
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
    "streamNamespace": "cluster('https://cdbfairfax.kusto.usgovcloudapi.net').database('LiveSite').OldJavaSDK",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDbUpgradeJavaSdk",
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
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/cosmosdb/sql-api-sdk-async-java",
  "description": "Upgrade your Azure Cosmos DB Java SDK to the latest version from Maven",
  "longDescription": "Your Azure Cosmos DB account is using an old version of the Java SDK. We recommend upgrading to the latest version from Maven for latest fixes, performance improvements, and new feature capabilities.",
  "potentialBenefits": "Improved reliability, performance, and new feature capabilities",
  "displayLabel": "Upgrade your Azure Cosmos DB Java SDK to the latest version from Maven",
  "additionalColumns": [
    {
      "name": "LatestVersion",
      "title": "Latest Version"
    }
  ],
  "actions": [
    {
      "actionId": "68e6f866-956c-4fd9-b16a-916222b663b6",
      "description": "Upgrade your Java SDK",
      "actionType": "Document",
      "documentLink": "https://aka.ms/cosmosdb/sql-api-sdk-async-java"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "7b999253-6a98-4f48-96c1-2852be4db70c",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  }
}
---
