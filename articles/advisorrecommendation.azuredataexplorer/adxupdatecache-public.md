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
  "version": 5.2,
  "learnMoreLink": "https://aka.ms/adxcachepolicy",
  "description": "(PREVIEW) Reduce Azure Data Explorer table cache-period (policy) for cluster cost optimization",
  "longDescription": "Reducing the table cache policy will free up Azure Data Explorer cluster nodes having low CPU utilization, memory, and a high cache size configuration",
  "potentialBenefits": "Optimize cost",
  "actions": [
	{
      "actionId": "B2F98EEC-E41A-44E2-8B80-1AB27EAC8B3B",
      "description": "Update cache settings",
      "actionType": "ContextBlade",
	  "extensionName": "Microsoft_Azure_Kusto",
      "bladeName": "CacheRecommendationBlade",
      "metadata": {
        "resource": "{resourceId}",
        "databaseName": "{databaseName}",
        "tableName": "{tableName}",
        "recommendedCachePolicy": "{recommendedCachePolicy}",
        "activeCachePolicy": "{currentCachePolicy}",
        "observationEndTime": "{ObservationEndTime}",
        "recommendationAnalysisTimespan": "{RecommendationAnalysisTimespan}",
        "description": "{description}"
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
  "costSavingInfo": "*Your actual yearly savings may vary. The yearly saving that is presented is based on 'pay as you go' prices. The potential saving does not take into consideration Azure Reserved VM Instances (RIs) billing discounts you may have.",
  "testData": "1f0d19a6-ad7b-45e9-b1c1-67aecd73046c,/subscriptions/1f0d19a6-ad7b-45e9-b1c1-67aecd73046c/resourceGroups/test/providers/Microsoft.Kusto/Clusters/autoradeprod,\"{\"\"potentialInstancesSave\"\": \"\"0.59\"\",\"\"potentialDataSavings\"\": \"\"1030.85 GB\"\",\"\"databaseName\"\": \"\"0658b4c418b746b0a74dac638339fc07\"\",\"\"tableName\"\": \"\"player_added_title\"\",\"\"currentConfig\"\": \"\"14 day(s)\"\",\"\"recommendedConfig\"\": \"\"86 day(s)\"\",\"\"cacheUsage\"\": \"\"95.0% of queries look back 86 day(s) or less. (1 queries were analyzed)\"\",\"\"observationWindow\"\": \"\"30 day(s)\"\",\"\"_stableIdToken\"\": \"\"/subscriptions/da6ebc03-a447-4930-805d-50d3953dcd01/resourceGroups/InsightsIngestionClusters.Roblox/providers/Microsoft.Kusto/clusters/pfextroblox001/Databases/0658b4c418b746b0a74dac638339fc07/Tables/player_added_title\"\",\"\"scaleAutomationSettingsEnabled\"\": \"\"false\"\",\"\"scaleAutomationSettingsMaxInstancesCount\"\": \"\"25\"\",\"\"scaleAutomationSettingsMinInstancesCount\"\": \"\"2\"\",\"\"scaleAutomationSettingsScaleOutRestrictionExpiresOn\"\": \"\"null\"\",\"\"scaleAutomationSettingsScaleInRestrictionExpiresOn\"\": \"\"null\"\",\"\"description\"\": \"\"Low usage table. 95% of queries look back 86 days or less (1 queries were analyzed). Consider deleting the table. (*) The analysis is based only on queries that scanned data.\"\",\"\"ObservationEndTime\"\": \"\"2021-03-10T12:00:00.1466709Z\"\",\"\"RecommendationAnalysisTimespan\"\": \"\"30.00:00:00\"\",\"\"currentCachePolicy\"\": \"\"14.00:00:00\"\",\"\"recommendedCachePolicy\"\": \"\"86.00:00:00\"\",\"\"requiredDataReductionForScaleIn\"\": \"\"1721.44 GB\"\"}\""
}
---
