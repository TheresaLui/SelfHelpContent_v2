<properties
    pageTitle="Configure Consistent indexing mode on your Azure Cosmos DB container"
    description="Configure Consistent indexing mode on your Azure Cosmos DB container"
    authors="pratnala"
    ms.author="pratnala"
    articleId="213974c8-ed9c-459f-9398-7cdaa3c28856_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Configure Consistent indexing mode on your Azure Cosmos DB container
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "213974c8-ed9c-459f-9398-7cdaa3c28856",
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDbLazyIndexing",
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
  "learnMoreLink": "https://docs.microsoft.com/azure/cosmos-db/how-to-manage-indexing-policy",
  "description": "Configure Consistent indexing mode on your Azure Cosmos DB container",
  "longDescription": "We noticed that your Azure Cosmos DB container is configured with the Lazy indexing mode, which may impact the freshness of query results. We recommend switching to Consistent mode.",
  "potentialBenefits": "Improve query result consistency and reliability",
  "displayLabel": "Configure Consistent indexing mode on your Azure Cosmos DB container",
  "dataSourceMetadata": {
    "dataSource": "Kusto",
    "streamNamespace": "cluster('https://cdbfairfax.kusto.usgovcloudapi.net').database('LiveSite').LazyIndexing",
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
      "actionId": "e98bcb9c-c554-46c5-81db-03483f8f38b2",
      "description": "Configure consistent indexing mode",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/cosmos-db/how-to-manage-indexing-policy"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "c74a0052-a732-453d-99c3-825671956207",
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
