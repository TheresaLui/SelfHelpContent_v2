<properties
    pageTitle="Update your Storage Data Movement Library to the latest version"
    description="Update your Storage Data Movement Library to the latest version"
    authors="yinfan"
    ms.author="xdataanalytics"
    articleId="02cfb5ef-z9b0-3522-8743-142gceb10057_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="StorageMediaEdge_XStore"
/>
# Sample title
---
{
  "recommendationOfferingId": "c3c3299d-ee34-4610-844d-3782d691a7fe",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "7e9fbfe8-1234-435c-b114-424445c9be6f",
  "dataSourceMetadata": {
    "streamNamespace": "AzureStorage.Data.AzureStorageAdvisorUseLatestVersionSDK_DMLib_FairfaxV2",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Storage/storageAccounts",
  "recommendationFriendlyName": "UpdateStorageDataMovementSDK",
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
  "learnMoreLink": "https://aka.ms/AA5wtca",
  "description": "Upgrade your Storage Client Library to the latest version for better reliability and performance",
  "longDescription": "The latest version of Storage Client Library/ SDK contains fixes to issues reported by customers and proactively identified through our QA process. The latest version also carries reliability and performance optimization in addition to new features that can improve your overall experience using Azure Storage.",
  "potentialBenefits": "Latest Storage Client Library contains fixes for known issues and additional improvements.",
  "supportedSDKLanguages": [".Net"],
  "actions": [
    {
      "actionId": "7e9fbfe8-1234-435c-b114-424445c9be7f",
      "description": "Learn how to update your Storage Data Movement Library",
      "actionType": "Document",
      "documentLink": "{recommendedActionLearnMore}"
    },
    {
      "actionId": "7e9fbfe8-1234-435c-b114-424445c9be8f",
      "description": "View {version} release notes",
      "actionType": "Document",
      "documentLink": "{releaseNotes}"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "7e9fbfe8-1234-435c-b114-424445c9be9f",
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
      "name": "language",
      "title": "SDK Language"
    },
    {
      "name": "version",
      "title": "Minimum Recommended Version"
    },
    {
      "name": "currentVersion",
      "title": "Current Version"
    }
  ],
  "tip": ""
}
---

