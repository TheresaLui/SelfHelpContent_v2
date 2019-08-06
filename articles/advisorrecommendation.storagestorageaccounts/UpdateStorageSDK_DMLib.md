<properties
    pageTitle="Update your Storage Data Movement Library to the latest version"
    description="Update your Storage Data Movement Library to the latest version"
    authors="yinfan"
    ms.author="xdataanalytics"
    articleId="02cfb5ef-z9b0-3522-8743-142gceb10057_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
/>
# Sample title
---
{
  "recommendationOfferingId": "c3c3299d-ee34-4610-844d-3782d691a7fe",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "02cfb5ef-z9b0-3522-8743-142gceb10057",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://xstore.kusto.windows.net') .database('xstore') .AzureStorageAdvisorUseLatestVersionSDK_DMLib",
    "dataSource": "Kusto",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Storage/storageAccounts",
  "recommendationFriendlyName": "UpdateSDK",
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
  "version": 1,
  "learnMoreLink": "",
  "description": "Upgrade your Storage Client Library to the latest version for better reliability and performance",
  "longDescription": "The latest version of Storage Client Library/ SDK contains fixes to issues reported by customers and proactively identified through our QA process. The latest version also carries reliability and performance optimization in addition to new features that can improve your overall experience using Azure Storage.",
  "potentialBenefits": "Latest Storage Client Library contains fixes for known issues and additional improvements.",
  "supportedSDKLanguages": [".Net"],
  "actions": [
    {
      "actionId": "184ffcd3-5ecc-52g4-0c5b-c5d58ff0423e",
      "description": "Learn how to update your Storage Data Movement Library",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/nuget/consume-packages/install-use-packages-visual-studio"
    },
    {
      "actionId": "184ffcd3-5ecc-52g4-0c5b-c5d58ff0423f",
      "description": "View {version} release notes",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Storage",
      "documentLink": "https://github.com/Azure/azure-storage-net-data-movement/releases/tag/v0.12.0"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "184ffcd3-5ecc-52g4-0c5b-c5d58ff0423g",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Storage",
      "bladeName": "StorageAccountBlade",
       "metadata": {
        "id": "{resourceId}"
      }
	}
  },
  "displayLabel": "Update Storage Data Movement Library",
  "additionalColumns": [
    {
      "name": "Language",
      "title": "SDK Language"
    },
    {
      "name": "Version",
      "title": "Minimum Recommended Version"
    }
  ],
  "tip": "",
  "testData": ""
}
---
