<properties
    pageTitle="Use Azure Lifecycle Management to Save Costs"
    description="Use Azure Lifecycle Management to Save Costs"
    authors="aadevteam" 
    ms.author="yuriic"
    articleId="700a6195-ddbc-42e9-9341-fa26f2039d96_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="StorageMediaEdge_XStore"
/>
# Utilize Lifecycle Management 
---
{
  "recommendationOfferingId": "4c4a2d61-b806-47af-a7ee-e8f8fcfce8bb",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "96d733d8-6d43-4340-ba9a-c7bbdef18f62",
  "dataSourceMetadata": {
    "streamNamespace": "AzureStorage.Data.StorageAdvisorLifecycleManagmentFairfaxV1",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Storage/storageAccounts",
  "recommendationFriendlyName": "LifecycleManagement",
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
  "version": 1.0,
  "description": "Use Lifecycle Management to transition older block blobs to a cooler tier.",
  "longDescription": "One or more of your storage accounts has a high number of block blobs that have been created at least 28 days ago with few transactions performed. Use Lifecycle Management rules to tier your data to Cool or Archive to optimize your storage costs while retaining your data in Azure blob storage for application compatibility.",
  "potentialBenefits": "Optimize your storage costs by migrating older block blobs to lower priced storage cost tiers like Cool or Archive.",
  "actions": [
    {
      "actionId": "2ee0f24a-9747-49e4-b4d0-cf929b48bdfe",
      "description": "Migrate data objects to a cooler tier using Data Lifecycle Management feature.",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}",
        "menuid": "managementPolicies"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "8615139e-0106-4611-a10c-e5b6c13b8e5a",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Create Lifecycle Management rules",
  "additionalColumns": [],
  "tip": "You can use Lifecycle Management to move block blobs with low transations to cooler tiers and optimize your storage costs.",
  "learnMoreLink": "https://docs.microsoft.com/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal",
  "testData": "8267c76e-43b7-4492-9475-cb555239c2f7,/subscriptions/8267c76e-43b7-4492-9475-cb555239c2f7/resourceGroups/mmmm/providers/Microsoft.Storage/storageAccounts/advisortest"
}
---
