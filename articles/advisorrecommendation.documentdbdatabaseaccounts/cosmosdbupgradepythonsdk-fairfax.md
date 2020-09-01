<properties
    pageTitle="Upgrade your Azure Cosmos DB Python SDK to the latest version from PyPI"
    description="Upgrade your Azure Cosmos DB Python SDK to the latest version from PyPI"
    authors="pratnala"
    ms.author="pratnala"
    articleId="b2fa566d-7da3-4c61-b35c-f2548c665aa0_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Upgrade your Azure Cosmos DB Python SDK to the latest version from PyPI
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "b2fa566d-7da3-4c61-b35c-f2548c665aa0",
  "dataSourceMetadata": {
    "dataSource": "Kusto",
    "streamNamespace": "cluster('https://cdbfairfax.kusto.usgovcloudapi.net').database('LiveSite').OldPythonSDK",
    "refreshInterval": "0.12:00:00",
    "schemaVersion": 3.0
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDbUpgradePythonSdk",
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
  "learnMoreLink": "https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-python",
  "description": "Upgrade your Azure Cosmos DB Python SDK to the latest version from PyPI",
  "longDescription": "Your Azure Cosmos DB account is using an old version of the Python SDK. We recommend upgrading to the latest version from PyPI for latest fixes, performance improvements, and new feature capabilities.",
  "potentialBenefits": "Improved reliability, performance, and new feature capabilities",
  "displayLabel": "Upgrade your Azure Cosmos DB Python SDK to the latest version from PyPI",
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
      "actionId": "2b5b95f9-7008-41fc-80e8-eb58a2f990ef",
      "description": "Upgrade your Python SDK",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/cosmos-db/sql-api-sdk-python"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "94f1e530-fae7-4963-b3fd-b5b6dbf40cbd",
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
