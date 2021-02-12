<properties
    pageTitle="Use Put Blob for blobs smaller than 256 MB"
    description="Use Put Blob for blobs smaller than 256 MB"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="b353f187-4cb4-4b2b-b502-472f45f32fd6_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="StorageMediaEdge_XStore"
/>
# Use Put Blob for blobs smaller than 256 MB
---
{
  "recommendationOfferingId": "c6b94711-f1f5-4e7e-9c89-c17ed4190969",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "b353f187-4cb4-4b2b-b502-472f45f32fd6",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "AzureStorageHUX.Data.StorageAdvisorOptimizeTX_PutBlob_Fairfax",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Storage/storageAccounts",
  "recommendationFriendlyName": "StorageCallPutBlob",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "xdataanalytics@microsoft.com",
    "icm": {
      "routingId": "mdm://XStore/DataAnalytics",
      "service": "Xstore",
      "team": "Xstore/ Data Analytics"
    },
    "serviceTreeId": "734379f9-2d2c-48d4-a52a-5c509f699de4"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "http://aka.ms/understandblockblobs",
  "description": "Use \"Put Blob\" for blobs smaller than 256 MB",
  "longDescription": "When writing a block blob that is 256 MB or less (64 MB for requests using REST versions before 2016-05-31), you can upload it in its entirety with a single write operation using \"Put Blob\". Based on your aggregated metrics, we believe your storage account's write operations can be optimized.",
  "potentialBenefits": "Increase performance and reduce operation costs.",
  "actions": [
    {
      "actionId": "e547abea-8f78-4e67-957b-a40bc8d454a4",
      "description": "Use \"Put Blob\" for Small Block Blobs",
      "actionType": "Document",
      "documentLink": "https://aka.ms/putblob"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "cdad8199-5dd1-414e-90ac-a48607ca4ab3",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Storage",
      "bladeName": "StorageAccountBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Optimize Block Blob Operations",
  "additionalColumns": []
}
---

