<properties
    pageTitle="Use larger block sizes for large block blob uploads"
    description="Use larger block sizes for large block blob uploads"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="70065997-d4d4-4671-baeb-39a2ac66e8ec_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="StorageMediaEdge_XStore"
/>
# Use larger block sizes for large block blob uploads
---
{
  "recommendationOfferingId": "c6b94711-f1f5-4e7e-9c89-c17ed4190969",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "70065997-d4d4-4671-baeb-39a2ac66e8ec",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "AzureStorageHUX.Data.StorageAdvisorOptimizeTX_LargerPutBlock",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Storage/storageAccounts",
  "recommendationFriendlyName": "StorageUseLargeBlockSizesForPutBlock",
  "recommendationMetadataState": "Disabled",
  "portalFeatures": [],
  "owner": {
    "email": "aadevteam@microsoft.com",
    "icm": {
      "routingId": "MDM://AzureAdvisor",
      "service": "Azure Advisor",
      "team": "Azure Advisor"
    },
    "serviceTreeId": "f6d7f416-ee14-4943-894b-1abca9140b74"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/understandblockblobs",
  "description": "Use larger block sizes for large block blob uploads",
  "longDescription": "When writing a block blob that is larger than 256 MB, using larger block sizes reduces the number of write operations required to upload the blob when calling \"Put Block\". Block blobs support up to 100 MB blocks for the REST API versions 2016-05-31 and later, and 4 MB for older versions. We suggest using at least 4 MB blocks when uploading large objects with the \"Put Block\" operation. Based on your aggregated metrics, we believe your storage account's write operations can be optimized.",
  "potentialBenefits": "Increase performance and reduce operation costs",
  "actions": [
    {
      "actionId": "aef31774-ec65-4882-9d31-4a369e4db565",
      "description": "Use Larger Block Sizes for \"Put Block\"",
      "actionType": "Document",
      "documentLink": "https://aka.ms/putblock"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "ab800bee-f8a5-453c-a8d4-475b3f999734",
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
