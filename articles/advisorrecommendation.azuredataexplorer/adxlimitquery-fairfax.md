<properties
    pageTitle="Update cache policies in Azure Data Explorer table"
    description="Update cache policies for Azure Data Explorer tables"
    authors="prvavill"
    ms.author="kustosee"
    articleId="33A981BE-795B-49EA-8E18-EE5795680BBF_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
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
    "streamNamespace": "cluster('https://kustodataestate.usgovvirginia.kusto.usgovcloudapi.net').database('AdvisorRecommendations').PublishLimitQueryRecommendations",
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
    "email": "kustosee@microsoft.com",
    "icm": {
      "routingId": "83b9306c-e434-4ec5-9bfc-a33b11e3eb19",
      "service": "Kusto",
      "team": "Kusto Live Incidents"
    },
    "serviceTreeId": "e02603c6-3469-498a-994c-b0df4ceae1d0"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 5.2,
  "learnMoreLink": "https://aka.ms/adxcachepolicy",
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
  ]
}
---
