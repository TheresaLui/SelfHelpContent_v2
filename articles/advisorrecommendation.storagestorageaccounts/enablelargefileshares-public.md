<properties
    pageTitle="Update your file share configuration to avoid throttling"
    description="Enable the large file share feature on storage account to avoid throttling. We noticed that more than 50% of your requests were throttled within a one hour period."
    authors="aadevteam"
    ms.author="xdataanalytics"
    articleId="dd65e838-4473-4fdb-b124-e09798e35f36_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, USSec, USNat"
    ownershipId="StorageMediaEdge_XStore"
/>
# Update your file share configuration to avoid throttling
---
{
  "recommendationOfferingId": "c3c3299d-ee34-4610-844d-3782d691a7fe",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "dd65e838-4473-4fdb-b124-e09798e35f36",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "AzureStorage.Data.StorageAdvisorEnableLargeFileSharesPublicV1_0",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Storage/storageAccounts",
  "recommendationFriendlyName": "EnableLargeFileShares",
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
  "version": 1.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/storage/files/storage-files-how-to-create-large-file-share#enable-large-files-shares-on-an-existing-account",
  "description": "Enable the large file share feature on storage account to avoid throttling.",
  "longDescription": "Standard file shares are limited to 1000 IOPS per share. By enabling the large file share feature you can get 10x more IOPS. There is no charge to enable large file shares. Enabling large files shares is an irreversible action. Large file shares enabled account can’t be converted to re-redundant accounts.",
  "potentialBenefits": "Eliminate throttling and improve the performance of your file shares.",
  "actions": [
    {
      "actionId": "312d30e2-6e24-43d4-934d-615a41d51eda",
      "description": "Enable the large file share feature on storage account to avoid throttling.",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/storage/files/storage-files-how-to-create-large-file-share#enable-large-files-shares-on-an-existing-account"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "173ef25a-1b4a-4f91-b549-0ed50501c7d5",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Storage",
      "bladeName": "StorageAccountBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Enable the large file share feature on storage account to avoid throttling",
  "additionalColumns": [],
  "testData": "65490f91-f2c2-4514-80ba-4ec1de89aeda,/subscriptions/65490f91-f2c2-4514-80ba-4ec1de89aeda/resourceGroups/XStoreDataAnalytics/providers/Microsoft.Storage/axdataanalyticsstgwcus",
  "tip": "By enabling the large file share feature you can get 10x more IOPS. There is no charge to enable large file shares.",
  "learnMoreLink": "https://docs.microsoft.com/azure/storage/files/storage-files-how-to-create-large-file-share#enable-large-files-shares-on-an-existing-account"
}
---
