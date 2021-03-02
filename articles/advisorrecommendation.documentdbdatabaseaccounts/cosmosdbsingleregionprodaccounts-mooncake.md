<properties
    pageTitle="Improve the availability of your production workloads on Azure Cosmos DB"
    description="Improve the availability of your production workloads on Azure Cosmos DB"
    authors="thweiss"
    ms.author="thweiss"
    articleId="b57f7a29-dcc8-43de-86fa-18d3f9d3764d_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Improve the availability of your production workloads on Azure Cosmos DB
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "b57f7a29-dcc8-43de-86fa-18d3f9d3764d",
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDBSingleRegionProdAccounts",
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
  "version": 1.0,
  "learnMoreLink": "https://docs.azure.cn/azure/cosmos-db/high-availability",
  "description": "Improve the availability of your production workloads on Azure Cosmos DB",
  "longDescription": "Based on their names and configuration, we have detected the Azure Cosmos DB accounts below as being potentially used for production workloads. These accounts currently run in a single Azure region. You can increase their availability by configuring them to span at least two Azure regions. <b>Note that additional regions will incur extra costs.</b>",
  "potentialBenefits": "Improve the availability of your production workloads",
  "displayLabel": "Improve the availability of your production workloads on Azure Cosmos DB",
  "dataSourceMetadata": {
    "dataSource": "Kusto",
    "streamNamespace": "cluster('https://cdbmooncake3.chinanorth2.kusto.chinacloudapi.cn').database('LiveSite').SingleRegionProdAccounts",
    "refreshInterval": "1.00:00:00"
  },
  "actions": [
    {
      "actionId": "5d04df30-9974-4b50-b1b9-e907c2ad3ce3",
      "description": "Consider adding a second Azure region",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_DocumentDB",
      "bladeName": "AddRemoveRegionsBlade",
      "metadata": {
        "resourceId": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "291d3a5a-9a3e-45f5-a40d-112fcec202db",
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
