<properties
    pageTitle="Reduce cache in Azure Data Explorer table"
    description="Reduce cache for Azure Data Explorer tables"
    authors="joaldaba"
    ms.author="aoaft"
    articleId="acb1c04d-975a-4649-80d6-6178765741c1_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureDataExplorer_Kusto"
/>
# The following Azure Data Explorer tables have been identified as candidates for updating their cache settings
---
{
  "recommendationOfferingId": "942bca88-3367-420f-a8c7-7eb34957f84d",
  "recommendationOfferingName": "Azure Data Explorer",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "947a627a-532d-44f8-8e23-4f365a80a2ba",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://kustodataestate.westeurope.kusto.windows.net').database('AdvisorRecommendations').PublishUpdateCacheRecommendations",
    "dataSource": "Kusto",
    "refreshInterval": "0.08:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Kusto/Clusters",
  "recommendationFriendlyName": "ReduceCacheForAzureDataExplorerTables",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "aoaft@microsoft.com",
    "icm": {
      "routingId": "AORECOMMENDATIONS\\Triage",
      "service": "AO Recommendations",
      "team": "Triage"
    },
    "serviceTreeId": "2edb14ce-371e-489a-9807-379870b819ef"
  },
  "ingestionClientIdentities": [
    "6c75c76c-7792-4dd0-8e85-ad598f14bc93",
    "db97364d-48bf-4567-af34-e0843d0ee0af",
    "bd26e40e-c0cc-4d1d-8801-569dac0cd7fe",
    "9c14bff5-1bda-4de6-a74f-4c3caa370570"
  ],
  "recommendationTimeToLive": 86400,
  "version": 4.1,
  "learnMoreLink": "https://aka.ms/adxcachepolicy",
  "description": "(PREVIEW) Reduce Azure Data Explorer table cache-period (policy) for cluster cost optimization",
  "longDescription": "Reducing the table cache policy will free up Azure Data Explorer cluster nodes having low CPU utilization, memory, and a high cache size configuration",
  "potentialBenefits": "Optimize cost",
  "actions": [
	{
      "actionId": "b5c42adb-3575-42e4-b0f6-fbfac584b362",
      "description": "Update cache settings",
      "actionType": "Blade",
	  "extensionName": "Microsoft_Azure_Kusto",
      "bladeName": "DatabaseOverviewBladeViewModel",
      "metadata": {
        "id": "{resourceId}"
      }
	}
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "72862f39-b75d-462f-b432-53a0f0dc37c7",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Cache Reduction - Consider setting your cache policy to the recommended value",
  "additionalColumns": [
    {
      "name": "databaseName",
      "title": "Database Name"
    },
	{
      "name": "tableName",
      "title": "Table Name"
    },
	{
      "name": "currentConfig",
      "title": "Current Cache Policy"
    },
	{
      "name": "cacheUsage",
      "title": "Current Usage"
    },
	{
      "name": "recommendedConfig",
      "title": "Recommended Cache Policy"
    },
	{
      "name": "potentialDataSavings",
      "title": "Estimated Data Savings"
    },
    {
      "name": "potentialInstancesSave",
      "title": "Potential Instances Save"
    },
	{
      "name": "requiredDataReductionForScaleIn",
      "title": "Required Data Reduction for Scale-In"
    },
	{
      "name": "observationWindow",
      "title": "Observation Window"
    }
  ],
  "costSavingInfo": "*Your actual yearly savings may vary. The yearly saving that is presented is based on 'pay as you go' prices. The potential saving does not take into consideration Azure Reserved VM Instances (RIs) billing discounts you may have."
}
---
