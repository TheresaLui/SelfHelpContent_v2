<properties
    pageTitle="Configure your Azure Cosmos DB applications to use Direct connectivity in the SDK"
    description="Configure your Azure Cosmos DB applications to use Direct connectivity in the SDK"
    authors="pratnala"
    ms.author="pratnala"
    articleId="75c8c891-46d2-41fa-a81c-84e870a139a9_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Configure your Azure Cosmos DB applications to use Direct connectivity in the SDK
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "75c8c891-46d2-41fa-a81c-84e870a139a9",
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDBGatewayMode",
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
  "learnMoreLink": "https://docs.azure.cn/cosmos-db/performance-tips#networking",
  "description": "Configure your Azure Cosmos DB applications to use Direct connectivity in the SDK",
  "longDescription": "We noticed that your Azure Cosmos DB applications are using Gateway mode via the Cosmos DB .NET or Java SDKs. We recommend switching to Direct connectivity for lower latency and higher scalability.",
  "potentialBenefits": "Improve latency and high availability of your applications",
  "displayLabel": "Configure your applications to use Direct connectivity in the SDK",
  "dataSourceMetadata": {
    "dataSource": "Kusto",
    "streamNamespace": "cluster('https://cdbmooncake3.chinanorth2.kusto.chinacloudapi.cn').database('LiveSite').GatewayMode",
    "refreshInterval": "0.12:00:01"
  },
  "actions": [
    {
      "actionId": "8d53c5ee-d517-4d13-8df8-cac65d6f5a56",
      "description": "Configure to use Direct connectivity",
      "actionType": "Document",
      "documentLink": "https://docs.azure.cn/cosmos-db/performance-tips#networking"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "b4f76069-a635-4dfa-a6bf-8fac5ff253e3",
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
