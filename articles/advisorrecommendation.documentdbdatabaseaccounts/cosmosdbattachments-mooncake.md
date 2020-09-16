<properties
    pageTitle="Migrate Azure Cosmos DB attachments to Azure Blob Storage"
    description="Migrate Azure Cosmos DB attachments to Azure Blob Storage"
    authors="andrl"
    ms.author="aliuy"
    articleId="061dcd4a-2090-4ec0-b4e0-ec9eaae5cf80_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Migrate Azure Cosmos DB attachments to Azure Blob Storage
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "41d957c1-1069-4190-8318-f80ab52c375f",
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDBAttachments",
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
  "learnMoreLink": "https://aka.ms/cosmosdb-attachments",
  "description": "Migrate Azure Cosmos DB attachments to Azure Blob Storage",
  "longDescription": "We noticed that your Azure Cosmos container is using the legacy attachments feature. We recommend migrating attachments to Azure Blob Storage to improve the resiliency and scalability of your blob data.",
  "potentialBenefits": "Improve attachment blob resiliency and scalability",
  "displayLabel": "Azure Cosmos DB attachments",
  "dataSourceMetadata": {
    "dataSource": "Kusto",
    "streamNamespace": "cluster('https://cdbmooncake3.chinanorth2.kusto.chinacloudapi.cn').database('LiveSite').Attachments",
    "refreshInterval": "0.04:00:00"
  },
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
      "actionId": "8cd46458-6e4a-4b0d-bde6-e65fd2381a5d",
      "description": "Migrate attachments",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/cosmos-db/attachments#migrating-attachments-to-azure-blob-storage"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "45ead073-2fd8-4d7b-8224-2b9a715c70a1",
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
