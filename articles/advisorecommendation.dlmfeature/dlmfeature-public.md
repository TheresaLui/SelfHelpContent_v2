<properties
    pageTitle="Use Azure Lifecycle Management to Save Costs"
    description="Use Azure Lifecycle Management to Save Costs"
    authors="xyh1" 
    ms.author="hux"
    articleId="700a6195-ddbc-42e9-9341-fa26f2039d96_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
/>
# Utilize Lifecycle Management 
---
{
  "recommendationOfferingId": "4c4a2d61-b806-47af-a7ee-e8f8fcfce8bb",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "96d733d8-6d43-4340-ba9a-c7bbdef18f62",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "cluster('https://xstore.kusto.windows.net').database('Xstore').azurestorageadvisorusedlm",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Storage/storageAccounts/",
  "recommendationFriendlyName": "LifecycleManagement",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "hux@microsoft.com, Sijia.Zhu@microsoft.com",
    "icm": {
      "routingId": "MDM://AzureAdvisor",
      "service": "Azure Advisor",
      "team": "Azure Advisor"
    },
    "serviceTreeId": "c77cbc0e-e61d-4aa0-9672-b63d529eac77"
  },
  "ingestionClientIdentities": [],
  "version": 1.0,
  "learnMoreLink": "https://docs.microsoft.com/en-us/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal",
  "description": "Utilize Lifecycle Management to transition older block blobs to a cooler tier.",
  "longDescription": "Detailed Description 
                    Your Storage account has few block blob transactions with a high number of blobs that have been created at least 28 days ago.  
                    Use Lifecycle Management rules to tier your data to Cool or Archive and decrease your storage costs while retaining your data in Azure Blob storage for application compatibility.",
  "potentialBenefits": "Decrease your storage costs by migrating older block blobs to lower priced storage cost tiers such as Cool or Archive.",
  "actions": [
    {
      "actionId": "2ee0f24a-9747-49e4-b4d0-cf929b48bdfe",
      "description": "Utilize Lifecycle Management to transition older block blobs to a cooler tier.",
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
  "displayLabel": "Use Lifecycle Management",
  "additionalColumns": [],
  "tip": "You can use Lifecycle Management to move block blobs with low transations to cooler tiers and decrease your storage costs.",
  "learnMoreLink": "https://docs.microsoft.com/en-us/azure/storage/blobs/storage-lifecycle-management-concepts?tabs=azure-portal"
  "testData": "8267c76e-43b7-4492-9475-cb555239c2f7,/subscriptions/8267c76e-43b7-4492-9475-cb555239c2f7/resourceGroups/mmmm/providers/Microsoft.Storage/storageAccounts/advisortest"
}
