<properties
    pageTitle="Configure Consistent indexing mode on your Azure Cosmos container"
    description="Configure Consistent indexing mode on your Azure Cosmos container"
    authors="pratnala"
    ms.author="pratnala"
    articleId="213974c8-ed9c-459f-9398-7cdaa3c28856_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Configure Consistent indexing mode on your Azure Cosmos container
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "213974c8-ed9c-459f-9398-7cdaa3c28856",
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDBLazyIndexing",
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
  "learnMoreLink": "https://docs.azure.cn/cosmos-db/how-to-manage-indexing-policy",
  "description": "Configure Consistent indexing mode on your Azure Cosmos container",
  "longDescription": "We noticed that your Azure Cosmos container is configured with the Lazy indexing mode, which may impact the freshness of query results. We recommend switching to Consistent mode.",
  "potentialBenefits": "Improve query result consistency and reliability",
  "displayLabel": "Configure Consistent indexing mode on your Azure Cosmos container",
  "dataSourceMetadata": {
    "dataSource": "Kusto",
    "streamNamespace": "cluster('https://cdbmooncake3.chinanorth2.kusto.chinacloudapi.cn').database('LiveSite').LazyIndexing",
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
      "documentLink": "https://docs.azure.cn/cosmos-db/how-to-manage-indexing-policy"
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
