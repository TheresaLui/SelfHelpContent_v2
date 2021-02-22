<properties
    pageTitle="Upgrade your outdated Azure Cosmos DB SDK to the latest version"
    description="Upgrade your outdated Azure Cosmos DB SDK to the latest version"
    authors="pratnala"
    ms.author="pratnala"
    articleId="60a55165-9ccd-4536-81f6-e8dc6246d3d2_USNat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USNat"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Upgrade your outdated Azure Cosmos DB SDK to the latest version
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "60a55165-9ccd-4536-81f6-e8dc6246d3d2",
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.DocumentDb/databaseAccounts",
  "recommendationFriendlyName": "CosmosDBUpgradeOutdatedSDK",
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
  "version": 2.1,
  "learnMoreLink": "https://docs.microsoft.com/azure/cosmos-db/",
  "description": "Upgrade your outdated Azure Cosmos DB SDK to the latest version",
  "longDescription": "Your Azure Cosmos DB account is using an outdated version of the SDK. We recommend upgrading to the latest version for the latest fixes, performance improvements, and new feature capabilities.",
  "potentialBenefits": "Improved reliability, performance, and new feature capabilities",
  "displayLabel": "Upgrade your outdated Azure Cosmos DB SDK to the latest version",
  "supportedSDKLanguages": [".NET", ".NET Core", "Sync Java", "Async Java", "Java", "Node.js", "Python", "Spark Connector"],
  "dataSourceMetadata": {
    "dataSource": "Kusto",
    "streamNamespace": "cluster('https://cdbusnateast.usnateast.kusto.core.eaglex.ic.gov').database('Support').OutdatedSDK",
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
      "actionId": "d5f51e69-66dc-4c66-a949-2d205468c5c3",
      "description": "Upgrade your {language} SDK",
      "actionType": "Document",
      "documentLink": "{recommendedActionLearnMore}"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "04475f2f-cf82-4edb-9be4-20724369962c",
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
