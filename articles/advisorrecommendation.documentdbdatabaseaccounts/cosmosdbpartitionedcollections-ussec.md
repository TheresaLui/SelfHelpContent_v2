<properties
    pageTitle="Configure your Azure Cosmos containers with a partition key"
    description="Configure your Azure Cosmos containers with a partition key"
    authors="pratnala"
    ms.author="pratnala"
    articleId="5b5349fb-b298-41e3-b281-982b7986db67_USSec"
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
  "recommendationTypeId": "5b5349fb-b298-41e3-b281-982b7986db67",
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDBPartitionedCollections",
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
  "version": 1.1,
  "learnMoreLink": "https://docs.microsoft.com/azure/cosmos-db/partitioning-overview#choose-partitionkey",
  "description": "Configure your Azure Cosmos containers with a partition key",
  "longDescription": "Your Azure Cosmos non-partitioned collections are approaching their provisioned storage quota. Please migrate these collections to new collections with a partition key definition so that they can automatically be scaled out by the service.",
  "potentialBenefits": "Scale your containers seamlessly with increase in storage or request rates without running into any limits",
  "displayLabel": "Configure your Azure Cosmos DB containers with a partition key",
  "dataSourceMetadata": {
    "dataSource": "Kusto",
    "streamNamespace": "cluster('https://cdbusseceast.usseceast.kusto.core.microsoft.scloud').database('Support').PartitionedCollections",
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
      "actionId": "89b9f16e-bf15-4247-a5dc-5f58f366459c",
      "description": "Configure containers with a partition key",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/cosmos-db/partitioning-overview#choose-partitionkey"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "2847eab2-874f-45b1-8517-a5e5709ef280",
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
