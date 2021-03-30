<properties
    pageTitle="Review the configuration of your Azure Cosmos DB free tier account"
    description="Review the configuration of your Azure Cosmos DB free tier account"
    authors="thweiss"
    ms.author="thweiss"
    articleId="4a993d7c-9d83-4d85-b5a9-7cce0b136378_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Review the configuration of your Azure Cosmos DB free tier account
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "4a993d7c-9d83-4d85-b5a9-7cce0b136378",
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDBFreeTierOverage",
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
  "version": 1.4,
  "learnMoreLink": "https://docs.azure.cn/azure/cosmos-db/understand-your-bill#azure-free-tier",
  "description": "Review the configuration of your Azure Cosmos DB free tier account",
  "longDescription": "Your Azure Cosmos DB free tier account is currently containing resources with a total provisioned throughput exceeding 400 Request Units per second (RU/s). Because Azure Cosmos DB's free tier only covers the first 400 RU/s of throughput provisioned across your account, any throughput beyond 400 RU/s will be billed at the regular pricing. As a result, we anticipate that you will get charged for the throughput currently provisioned on your Azure Cosmos DB account.",
  "potentialBenefits": "Confirm your expected Azure Cosmos DB costs",
  "displayLabel": "Review the configuration of your Azure Cosmos DB free tier account",
  "dataSourceMetadata": {
    "dataSource": "Kusto",
    "streamNamespace": "cluster('https://cdbmooncake3.chinanorth2.kusto.chinacloudapi.cn').database('LiveSite').FreeTierOverage",
    "refreshInterval": "0.04:00:00"
  },
  "additionalColumns": [
    {
      "name": "averageHourlyProvisionedThroughput",
      "title": "Average hourly provisioned throughput"
    },
    {
      "name": "regionCount",
      "title": "Region count"
    },
    {
      "name": "databaseCount",
      "title": "Database count"
    },
    {
      "name": "containerCount",
      "title": "Container count"
    }
  ],
  "actions": [
    {
      "actionId": "652fb6d8-a9c8-449e-9251-0e4649d683ea",
      "description": "Review your current and forecasted costs",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_CostManagement",
      "bladeName": "CostAnalysis",
      "metadata": {
        "scope": "{resourceGroupPath}"
      }
    },
    {
      "actionId": "17e095c0-ba6a-47d0-978c-f986c574b479",
      "description": "Explore all resources created in your account",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_DocumentDB",
      "bladeName": "DataExplorerBlade",
      "metadata": {
        "resourceId": "{resourceId}",
        "kind": null
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "ea9f1ac3-b968-471d-9b4a-071849a34e6e",
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
