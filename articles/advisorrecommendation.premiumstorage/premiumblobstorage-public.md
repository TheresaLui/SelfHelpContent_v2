<properties
    pageTitle="Create an Azure Premium Storage alert"
    description="Create an Azure Premium Storage alert"
    authors="xyh1" 
    ms.author="hux"
    articleId="7393910d-8cca-4b4b-957c-f53d79a5cd70_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="StorageMediaEdge_XStore"
/>
# Use Premium Blobs for block blob storage
---
{
  "recommendationOfferingId": "5b32eaf4-73d5-4a36-8468-74cbf71b11f5",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "c6b94711-f1f5-4e7e-9c89-c17ed4190969",
  "dataSourceMetadata": {
    "streamNamespace": "AzureStorage.Data.StorageAdvisorPremiumBlobStorageAccountV1",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Storage/storageAccounts",
  "recommendationFriendlyName": "PremiumBlobStorageAccount",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "Sijia.Zhu@microsoft.com",
    "icm": {
      "routingId": "MDM://AzureAdvisor",
      "service": "Azure Advisor",
      "team": "Azure Advisor"
    },
    "serviceTreeId": "e58a942f-58e5-49c3-9798-cbd6819f5cc0"
  },
  "ingestionClientIdentities": [],
  "version": 1.0,
  "description": "Use premium performance block blob storage",
  "longDescription": "One or more of your storage accounts has a high transaction rate per GB of block blob data stored. Use premium performance block blob storage instead of standard performance storage for your workloads that require fast storage response times and/or high transaction rates and potentially save on storage costs.",
  "potentialBenefits": "Block blob storage performance boost with the lowest Azure transaction prices.",
  "actions": [
    {
      "actionId": "f8db3c62-8ed7-48ea-b313-83c7224a5c47",
      "description": "Use premium performance block blob storage",
      "actionType": "Document",
      "extensionName": "Microsoft_Azure_Monitoring",
      "documentLink": "https://docs.microsoft.com/azure/storage/blobs/storage-blob-create-account-block-blob?tabs=azure-portal"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "9c19a87a-7f97-461b-9675-486c92c79ca8",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Use premium performance block blob storage",
  "additionalColumns": [],
  "tip": "You can use Premium Blobs on high transaction blobs to boost performance.",
  "learnMoreLink": "https://aka.ms/usePremiumBlob",
  "testData": "8267c76e-43b7-4492-9475-cb555239c2f7,/subscriptions/8267c76e-43b7-4492-9475-cb555239c2f7/resourceGroups/mmmm/providers/Microsoft.Storage/storageAccounts/advisortest"
}
---
