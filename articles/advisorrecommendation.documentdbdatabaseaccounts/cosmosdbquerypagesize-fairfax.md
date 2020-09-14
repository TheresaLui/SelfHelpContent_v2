<properties
    pageTitle="Configure your Azure Cosmos DB query page size (MaxItemCount) to -1"
    description="Configure your Azure Cosmos DB query page size (MaxItemCount) to -1"
    authors="pratnala"
    ms.author="pratnala"
    articleId="e27c5181-5005-4dc3-a449-89b726a3bf54_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Configure your Azure Cosmos DB query page size (MaxItemCount) to -1
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "e27c5181-5005-4dc3-a449-89b726a3bf54",
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDBQueryPageSize",
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
  "learnMoreLink": "https://docs.microsoft.com/azure/cosmos-db/sql-api-query-metrics#max-item-count",
  "description": "Configure your Azure Cosmos DB query page size (MaxItemCount) to -1",
  "longDescription": "You are using the query page size of 100 for queries for your Azure Cosmos container. We recommend using a page size of -1 for faster scans.",
  "potentialBenefits": "End to end query latency will be improved significantly",
  "displayLabel": "Configure your Azure Cosmos DB query page size (MaxItemCount) to -1",
  "dataSourceMetadata": {
    "dataSource": "Kusto",
    "streamNamespace": "cluster('https://cdbfairfax.kusto.usgovcloudapi.net').database('LiveSite').QueryPageSize",
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
      "actionId": "29039a89-7db5-44c6-b8f9-cc2cc021e93d",
      "description": "Use a page size of -1",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/cosmos-db/sql-api-query-metrics#max-item-count"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "f0a1b121-2642-4c0a-91aa-6ca4e5e5463b",
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
