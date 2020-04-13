<properties
    pageTitle="Configure your Azure Cosmos DB indexing policy with custom included or excluded paths"
    description="Configure your Azure Cosmos DB indexing policy with custom included or excluded paths"
    authors="rnagpal"
    ms.author="rnagpal"
    articleId="0fd5e55f-2338-4bf0-ad08-c37870c5d437_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Configure your Azure Cosmos DB indexing policy with custom included or excluded paths
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "0fd5e55f-2338-4bf0-ad08-c37870c5d437",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDbHighIndexingRUs",
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
  "ingestionClientIdentities": [
    "6c75c76c-7792-4dd0-8e85-ad598f14bc93",
    "db97364d-48bf-4567-af34-e0843d0ee0af",
    "bd26e40e-c0cc-4d1d-8801-569dac0cd7fe"
  ],
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/cosmosdb/modify-index-policy",
  "description": "Configure your Azure Cosmos DB indexing policy with custom included or excluded paths",
  "longDescription": "You are using the default indexing policy for your Azure Cosmos DB container which indexes all properties. Based on your workload patterns, we recommend using a custom indexing policy with explicit included or excluded paths used in query filters, in order to reduce the RUs and storage consumed for indexing.",
  "potentialBenefits": "Lower index RU utilization and storage size consumed per container",
  "displayLabel": "Configure your Azure Cosmos DB indexing policy with custom included or excluded paths",
  "additionalColumns": [
    {
      "name": "databaseName",
      "title": "Database"
    },
    {
      "name": "containerName",
      "title": "Container"
    }
  ],
  "actions": [
    {
      "actionId": "2dd93028-47fc-4dc8-bc14-f00b86f52352",
      "description": "Use a custom index policy",
      "actionType": "Document",
      "documentLink": "https://aka.ms/cosmosdb/modify-index-policy"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "dc1c28c2-39cf-4632-a028-eceee32060a5",
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
