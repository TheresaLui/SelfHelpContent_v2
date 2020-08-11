<properties
    pageTitle="Upgrade your old Azure Cosmos DB SDK to the latest version"
    description="Upgrade your old Azure Cosmos DB SDK to the latest version"
    authors="pratnala"
    ms.author="pratnala"
    articleId="51a4e6bd-5a95-4a41-8309-40f5640fdb8b_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Upgrade your old Azure Cosmos DB SDK to the latest version
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "51a4e6bd-5a95-4a41-8309-40f5640fdb8b",
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DocumentDb/databaseAccounts",
  "recommendationFriendlyName": "CosmosDBUpgradeOldSDK",
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
  "learnMoreLink": "https://docs.microsoft.com/azure/cosmos-db/",
  "description": "Upgrade your old Azure Cosmos DB SDK to the latest version",
  "longDescription": "Your Azure Cosmos DB account is using an old version of the SDK. We recommend upgrading to the latest version for the latest fixes, performance improvements, and new feature capabilities.",
  "potentialBenefits": "Improved reliability, performance, and new feature capabilities",
  "displayLabel": "Upgrade your old Azure Cosmos DB SDK to the latest version",
  "supportedSDKLanguages": [".NET", ".NET Core", "Sync Java", "Async Java", "Java", "Node.js", "Python"],
  "dataSourceMetadata": {
    "dataSource": "Kusto",
    "streamNamespace": "cluster('https://cdbsupport.kusto.windows.net').database('Support').OldSDK",
    "refreshInterval": "0.03:00:00"
  },
  "additionalColumns": [
    {
      "name": "language",
      "title": "SDK Language"
    },
    {
      "name": "currentVersion",
      "title": "Current Version"
    },
    {
      "name": "version",
      "title": "Recommended Version"
    }
  ],
  "actions":[
    {
      "actionId": "4d0763f5-4225-492e-9b2d-40de0994c098",
      "description": "Upgrade your {language} SDK",
      "actionType": "Document",
      "documentLink": "{recommendedActionLearnMore}"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "fef02123-5f0a-4c34-b927-eb8e63d5eaef",
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
