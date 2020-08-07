<properties
    pageTitle="Upgrade your Azure Cosmos DB .NET SDK to the latest version from Nuget"
    description="Upgrade your Azure Cosmos DB .NET SDK to the latest version from Nuget"
    authors="pratnala"
    ms.author="pratnala"
    articleId="7632ec99-ea15-4a40-be58-81168381b665_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Upgrade your Azure Cosmos DB .NET SDK to the latest version from Nuget
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "7632ec99-ea15-4a40-be58-81168381b665",
  "dataSourceMetadata": {
    "dataSource": "Kusto",
    "streamNamespace": "cluster('https://cdbmooncake3.chinanorth2.kusto.chinacloudapi.cn').database('LiveSite').OldDotNetSDK",
    "refreshInterval": "0.12:00:00",
    "schemaVersion": 3.0
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDbUpgradeDotNetSdk",
  "recommendationMetadataState": "Disabled",
  "owner": {
    "email": "cosmosnotifications@microsoft.com",
    "icm": {
      "routingId": "mdm://adspartner/CosmosDb",
      "service": "Azure Cosmos DB",
      "team": "Supportability"
    },
    "serviceTreeId": "724c33bf-1ab8-4691-adb1-0e61932919c2"
  },
  "version": 2.6,
  "learnMoreLink": "https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-dotnet-standard",
  "description": "Upgrade your Azure Cosmos DB .NET SDK to the latest version from Nuget",
  "longDescription": "Your Azure Cosmos DB account is using an old version of the .NET SDK. We recommend upgrading to the latest version from Nuget for latest fixes, performance improvements, and new feature capabilities.",
  "potentialBenefits": "Improved reliability, performance, and new feature capabilities",
  "displayLabel": "Upgrade your Azure Cosmos DB .NET SDK to the latest version from Nuget",
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
      "actionId": "f73e70bf-eb0e-441c-b59d-c057612bd7e6",
      "description": "Upgrade your .NET SDK",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-dotnet-standard"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "40731314-8a80-4229-9e17-8250a7921987",
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
