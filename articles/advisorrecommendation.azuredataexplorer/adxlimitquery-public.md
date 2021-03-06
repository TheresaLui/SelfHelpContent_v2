<properties
    pageTitle="Update cache policies in Azure Data Explorer table"
    description="Update cache policies for Azure Data Explorer tables"
    authors="joaldaba"
    ms.author="aoaft"
    articleId="d437a3b5-c7a2-4162-83a2-ba8e7ce18d99_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureDataExplorer_Kusto"
/>
# The following Azure Data Explorer tables have been identified as candidates for updating their cache settings
---
{
  "recommendationOfferingId": "0b85c950-0437-4844-be0e-dbbeced43ae5",
  "recommendationOfferingName": "Azure Data Explorer",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "f011adf6-475a-48c9-bf26-8db051cb6964",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://kustodataestate.westeurope.kusto.windows.net').database('AdvisorRecommendations').PublishLimitQueryRecommendations",
    "dataSource": "Kusto",
    "refreshInterval": "0.08:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Kusto/Clusters",
  "recommendationFriendlyName": "UpdateCachePoliciesForAdxTables",
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
  "learnMoreLink": "https://aka.ms/adxcacheperformance",
  "description": "(PREVIEW) Review Azure Data Explorer table cache-period (policy) for better performance",
  "longDescription": "This recommendation surfaces Azure Data Explorer tables which have a high number of queries that look back beyond the configured cache period (policy) (You will see the top 10 tables by query percentage that access out-of-cache data). The recommended action to improve the cluster's performance: Limit queries on this table to the minimal necessary time range (within the defined policy). Alternatively, if data from the entire time range is required, increase the cache period to the recommended value.",
  "potentialBenefits": "Optimize performance",
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
      "actionId": "f702dbb7-6a38-41ed-ab6e-1af313ad260e",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Query time range is too wide - Consider setting your cache period (policy) to the recommended value",
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
      "title": "Current Cache Period"
    },
	{
      "name": "cacheUsage",
      "title": "Current Usage"
    },
	{
      "name": "recommendedConfig",
      "title": "Recommended Cache Period"
    },
	{
      "name": "observationWindow",
      "title": "Observation Window"
    }
  ],
  "testData": "1f0d19a6-ad7b-45e9-b1c1-67aecd73046c,/subscriptions/1f0d19a6-ad7b-45e9-b1c1-67aecd73046c/resourceGroups/test/providers/Microsoft.Kusto/Clusters/autoradeprod,\"{\"\"databaseName\"\": \"\"0658b4c418b746b0a74dac638339fc07\"\",\"\"tableName\"\": \"\"player_added_title\"\",\"\"currentConfig\"\": \"\"14 day(s)\"\",\"\"recommendedConfig\"\": \"\"86 day(s)\"\",\"\"cacheUsage\"\": \"\"95.0% of queries look back 86 day(s) or less. (1 queries were analyzed)\"\",\"\"observationWindow\"\": \"\"30 day(s)\"\",\"\"_stableIdToken\"\": \"\"/subscriptions/da6ebc03-a447-4930-805d-50d3953dcd01/resourceGroups/InsightsIngestionClusters.Roblox/providers/Microsoft.Kusto/clusters/pfextroblox001/Databases/0658b4c418b746b0a74dac638339fc07/Tables/player_added_title\"\",\"\"scaleAutomationSettingsEnabled\"\": \"\"false\"\",\"\"scaleAutomationSettingsMaxInstancesCount\"\": \"\"25\"\",\"\"scaleAutomationSettingsMinInstancesCount\"\": \"\"2\"\",\"\"scaleAutomationSettingsScaleOutRestrictionExpiresOn\"\": \"\"null\"\",\"\"scaleAutomationSettingsScaleInRestrictionExpiresOn\"\": \"\"null\"\",\"\"description\"\": \"\"Low usage table. 95% of queries look back 86 days or less (1 queries were analyzed). Consider deleting the table. (*) The analysis is based only on queries that scanned data.\"\",\"\"ObservationEndTime\"\": \"\"2021-03-10T12:00:00.1466709Z\"\",\"\"RecommendationAnalysisTimespan\"\": \"\"30.00:00:00\"\",\"\"currentCachePolicy\"\": \"\"14.00:00:00\"\",\"\"recommendedCachePolicy\"\": \"\"86.00:00:00\"\"}\""
}
---
