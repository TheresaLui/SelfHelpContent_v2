<properties
    pageTitle="Configure your Azure Cosmos containers with a partition key"
    description="Configure your Azure Cosmos containers with a partition key"
    authors="pratnala"
    ms.author="pratnala"
    articleId="5e4e9f04-9201-4fd9-8af6-a9539d13d8ec_USSec"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USSec"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Configure your Azure Cosmos containers with a partition key
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "5e4e9f04-9201-4fd9-8af6-a9539d13d8ec",
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDBFixedCollections",
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
  "version": 2.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/cosmos-db/partitioning-overview#choose-partitionkey",
  "description": "Configure your Azure Cosmos containers with a partition key",
  "longDescription": "Your Azure Cosmos non-partitioned collections are approaching their provisioned storage quota. Please migrate these collections to new collections with a partition key definition so that they can automatically be scaled out by the service.",
  "potentialBenefits": "Scale your containers seamlessly with increase in storage or request rates without running into any limits",
  "displayLabel": "Configure your Azure Cosmos DB containers with a partition key",
  "dataSourceMetadata": {
    "dataSource": "Kusto",
    "streamNamespace": "cluster('https://cdbusseceast.usseceast.kusto.core.microsoft.scloud').database('Support').FixedCollections",
    "refreshInterval": "0.12:00:00"
  },
  "additionalColumns": [
    {
      "name": "databaseName",
      "title": "Database"
    },
    {
      "name": "collectionName",
      "title": "Collection"
    }
  ],
  "actions": [
    {
      "actionId": "a3427907-2ed2-4f9a-b16c-6bd450cdd57a",
      "description": "Configure containers with a partition key",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/cosmos-db/partitioning-overview#choose-partitionkey"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "06bd4d71-346a-40a6-9d6d-d916703436de",
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
