<properties
    pageTitle="Upgrade your Azure Cosmos DB Node.js SDK to the latest version from npm"
    description="Upgrade your Azure Cosmos DB Node.js SDK to the latest version from npm"
    authors="pratnala"
    ms.author="pratnala"
    articleId="ef3906d2-dcc4-43d0-aa5c-40e49a57de83_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Upgrade your Azure Cosmos DB Node.js SDK to the latest version from npm
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "ef3906d2-dcc4-43d0-aa5c-40e49a57de83",
  "dataSourceMetadata": {
    "dataSource": "Kusto",
    "streamNamespace": "cluster('https://cdbmooncake3.chinanorth2.kusto.chinacloudapi.cn').database('LiveSite').OldNodeJsSDK",
    "refreshInterval": "0.12:00:00",
    "schemaVersion": 3.0
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDbUpgradeNodeJsSdk",
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
  "version": 2.1,
  "learnMoreLink": "https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-node",
  "description": "Upgrade your Azure Cosmos DB Node.js SDK to the latest version from npm",
  "longDescription": "Your Azure Cosmos DB account is using an old version of the Node.js SDK. We recommend upgrading to the latest version from npm for latest fixes, performance improvements, and new feature capabilities.",
  "potentialBenefits": "Improved reliability, performance, and new feature capabilities",
  "displayLabel": "Upgrade your Azure Cosmos DB Node.js SDK to the latest version from npm",
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
      "actionId": "a2472632-15f0-44f1-ae7a-e394e6255dec",
      "description": "Upgrade your Node.js SDK",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-node"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "2e28cdd2-0c78-4a9e-8f5b-8df26aa6e403",
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
