<properties
    pageTitle="Enable Soft Delete to protect your blob data"
    description="Enable Soft Delete to protect your blob data"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="42dbf883-9e4b-4f84-9da4-232b87c4b5e9_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="StorageMediaEdge_XStore"
/>
# Enable Soft Delete to protect your blob data
---
{
  "recommendationOfferingId": "c6b94711-f1f5-4e7e-9c89-c17ed4190969",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "42dbf883-9e4b-4f84-9da4-232b87c4b5e9",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "AzureStorageHUX.Data.StorageAdvisorEnableSoftDelete_Fairfax",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Storage/storageAccounts",
  "recommendationFriendlyName": "StorageSoftDelete",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "hux@microsoft.com",
    "icm": {
      "routingId": "mdm://XStore/DataAnalytics",
      "service": "Xstore",
      "team": "Xstore/Data Analytics"
    },
    "serviceTreeId": "734379f9-2d2c-48d4-a52a-5c509f699de4"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/softdelete",
  "description": "Enable Soft Delete to protect your blob data",
  "longDescription": "After enabling Soft Delete, deleted data transitions to a soft deleted state instead of being permanently deleted. When data is overwritten, a soft deleted snapshot is generated to save the state of the overwritten data. You can configure the amount of time soft deleted data is recoverable before it permanently expires.",
  "potentialBenefits": "Save and recover your data when blobs or blob snapshots are accidentally overwritten or deleted",
  "actions": [
    {
      "actionId": "86df9c85-0d11-4468-b58a-34e1c745e252",
      "description": "Enable Soft Delete to protect blob data",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Storage",
      "bladeName": "DataProtectionBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "0574d759-144a-4fdc-9201-83370c3bd756",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Storage",
      "bladeName": "StorageAccountBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Enable Soft Delete",
  "additionalColumns": []
}
---

