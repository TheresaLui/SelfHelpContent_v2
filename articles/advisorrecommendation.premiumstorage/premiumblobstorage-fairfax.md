<properties
    pageTitle="Create an Azure Premium Storage alert"
    description="Create an Azure Premium Storage alert"
    authors="aadevteam" 
    ms.author="yuriic"
    articleId="c6b94711-f1f5-4e7e-9c89-c17ed4190969_FairFax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
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
    "streamNamespace": "AzureStorage.Data.StorageAdvisorPremiumBlobStorageAccountFairfaxV1",
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
      "routingId": "mdm://XStore/DataAnalytics",
      "service": "Xstore",
      "team": "Xstore/ Data Analytics"
    },
    "serviceTreeId": "734379f9-2d2c-48d4-a52a-5c509f699de4"
  },
  "ingestionClientIdentities": [],
  "version": 1.1,
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
