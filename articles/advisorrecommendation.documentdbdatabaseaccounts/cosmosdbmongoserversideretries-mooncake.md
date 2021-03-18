<properties
    pagetitle="Enable Server Side Retry (SSR) on your Azure Cosmos DB's API for MongoDB account"
    description="Enable Server Side Retry (SSR) on your Azure Cosmos DB's API for MongoDB account"
    authors="pratnala"
    ms.author="pratnala"
    articleId="ec6fe20c-08d6-43da-ac18-84ac83756a88_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Enable Server Side Retry (SSR) on your Azure Cosmos DB's API for MongoDB account
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "ec6fe20c-08d6-43da-ac18-84ac83756a88",
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDBMongoServerSideRetries",
  "recommendationMetadataState": "Active",
  "owner: {
    "email": "cosmosnotifications@microsoft.com",
    "icm": {
      "routingId": "mdm://adspartner/CosmosDb",
      "service": "Azure Cosmos DB",
      "team": "Supportability"
    },
    "serviceTreeId": "724c33bf-1ab8-4691-adb1-0e61932919c2",
  },
  "version": 1.0,
  "learnMoreLink": "https://docs.azure.cn/cosmos-db/prevent-rate-limiting-errors",
  "description": "Enable Server Side Retry (SSR) on your Azure Cosmos DB's API for MongoDB account",
  "longDescription": "We observed your account is throwing a TooManyRequests error with the 16500 error code. Enabling Server Side Retry (SSR) can help mitigate this issue for you.",
  "potentialBenefits": "Prevent throttling and improve your query reliability and performance",
  "displayLabel": "Enable Server Side Retry (SSR) on your Azure Cosmos DB's API for MongoDB account",
  "dataSourceMetadata: {
    "dataSource": "Kusto",
    "streamNamespace": "cluster('https://cdbmooncake3.chinanorth2.kusto.chinacloudapi.cn').database('LiveSite').MongoServerSideRetriesAdvisor",
    "refreshInterval": "0.12:00:00"
  },
  "actions: [
    {
      "actionId": "bf078cec-e092-439b-8663-47697464f362",
      "description": "Enable Server Side Retry (SSR)",
      "actionType": "Blade",
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "bf40eec6-d97d-45b8-a03c-e2faed3b0fb1",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_DocumentDB",
      "bladeName": "MongoAccountTemplateBlade",
      "metadata": {
        "": "{resourceId}"
      }
    }
  }
---

