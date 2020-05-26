<properties
    pageTitle="Update your Storage Client Library to the latest version"
    description="Update your Storage Client Library to the latest version"
    authors="yinfan"
    ms.author="xdataanalytics"
    articleId="13215084-d37f-41b3-889a-be66f24fd805_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="StorageMediaEdge_XStore"
/>
# Sample title
---
{
  "recommendationOfferingId": "c3c3299d-ee34-4610-844d-3782d691a7fe",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "97172837-e5ea-45b2-af3b-cadbf428a6d9",
  "dataSourceMetadata": {
    "streamNamespace": "AzureStorage.Data.AzureStorageAdvisorUseLatestVersionSDK_AllRoles_PublicV2",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Storage/storageAccounts",
  "recommendationFriendlyName": "UpdateStorageSDK",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "yinfan@microsoft.com",
    "icm": {
      "routingId": "mdm://XStore/DataAnalytics",
      "service": "Xstore",
      "team": "Xstore/ Data Analytics"
    },
    "serviceTreeId": "734379f9-2d2c-48d4-a52a-5c509f699de4"
  },
  "version": 3,
  "learnMoreLink": "{recommendedActionLearnMore}",
  "description": "Upgrade your Storage Client Library to the latest version for better reliability and performance",
  "longDescription": "The latest version of Storage Client Library/ SDK contains fixes to issues reported by customers and proactively identified through our QA process. The latest version also carries reliability and performance optimization in addition to new features that can improve your overall experience using Azure Storage.",
  "potentialBenefits": "Latest Storage Client Library contains fixes for known issues and additional improvements.",
  "supportedSDKLanguages": ["C++", ".Net"],
  "actions": [
    {
      "actionId": "3343ccda-2784-4e48-8421-86017676872c",
      "description": "Learn how to update your Storage Client Library",
      "actionType": "Document",
      "documentLink": "{recommendedActionLearnMore}"
    },
    {
      "actionId": "59a19528-6fd9-4a51-bf6a-1ea94c4bb36f",
      "description": "View {version} release notes",
      "actionType": "Document",
      "documentLink": "{releaseNotes}"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "1c5447d4-19c5-4cc9-93f7-19fd49180169",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Storage",
      "bladeName": "StorageAccountBlade",
       "metadata": {
        "id": "{resourceId}"
      }
	}
  },
  "displayLabel": "Update Storage Client Library",
  "additionalColumns": [
    {
      "name": "language",
      "title": "SDK Language"
    },
    {
      "name": "version",
      "title": "Minimum Recommended Version"
    }
  ],
  "tip": "",
  "testData": "65490f91-f2c2-4514-80ba-4ec1de89aeda, /subscriptions/65490f91-f2c2-4514-80ba-4ec1de89aeda/resourceGroups/XStoreDataAnalytics/providers/Microsoft.Storage/storageAccounts/axdataanalyticsstgwestus, \"{\"\"language\"\":\"\".Net\"\",\"\"version\"\":\"\"10.0.1\"\",\"\"recommendedActionLearnMore\"\":\"\"https://github.com/Azure/azure-storage-net/#via-nuget\"\",\"\"releaseNotes\"\":\"\"https://github.com/Azure/azure-storage-net/releases/tag/v10.0.2\"\"}\""
}
---
