<properties
    pageTitle="Reduce cache in Azure Data Explorer table"
    description="Reduce cache for Azure Data Explorer tables"
    authors="dsigron"
    ms.author="kustosee"
    articleId="9a3ea211-a282-4ab6-a63b-81024975b796_USSec"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USSec"
    ownershipId="AzureDataExplorer_Kusto"
/>
# The following Azure Data Explorer tables have been identified as candidates for updating their cache settings
---
{
  "recommendationOfferingId": "f69180f4-2eea-4124-a08d-c8ab3663a249",
  "recommendationOfferingName": "Azure Data Explorer",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "9a3ea211-a282-4ab6-a63b-81024975b796",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://kustodataestate.usseceast.kusto.core.microsoft.scloud').database('AdvisorRecommendations').PublishUpdateCacheExcellenceRecommendations",
    "dataSource": "Kusto",
    "refreshInterval": "0.08:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Kusto/Clusters",
  "recommendationFriendlyName": "ReduceCacheForAzureDataExplorerTablesOperationalExcellence",
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
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/adxcachepolicy",
  "description": "(PREVIEW)Reduce the cache policy on your Azure Data Explorer tables",
  "longDescription": "Reduce the table cache policy to match the usage patterns (query lookback period)",
  "potentialBenefits": "Cache reduction",
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
  "displayLabel": "Reduce the table cache policy to match the usage patterns (query lookback period)",
  "additionalColumns": [
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
      "name": "observationWindow",
      "title": "Observation Window"
    }
  ]
}
---
