<properties
    pageTitle="Migrate Azure Cosmos DB attachments to Azure Blob Storage"
    description="Migrate Azure Cosmos DB attachments to Azure Blob Storage"
    authors="andrl"
    ms.author="aliuy"
    articleId="061dcd4a-2090-4ec0-b4e0-ec9eaae5cf80_USNat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USNat"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Migrate Azure Cosmos DB attachments to Azure Blob Storage
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "061dcd4a-2090-4ec0-b4e0-ec9eaae5cf80",
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
  "learnMoreLink": "https://docs.microsoft.com/azure/cosmos-db/attachments#migrating-attachments-to-azure-blob-storage",
  "description": "Migrate Azure Cosmos DB attachments to Azure Blob Storage",
  "longDescription": "We noticed that your Azure Cosmos collection is using the legacy attachments feature. We recommend migrating attachments to Azure Blob Storage to improve the resiliency and scalability of your blob data.",
  "potentialBenefits": "Improve attachment blob resiliency and scalability",
  "displayLabel": "Migrate Azure Cosmos DB attachments to Azure Blob Storage",
  "dataSourceMetadata": {
    "dataSource": "Kusto",
    "streamNamespace": "cluster('https://cdbusnateast.usnateast.kusto.core.eaglex.ic.gov').database('Support').Attachments",
    "refreshInterval": "0.04:00:00"
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
