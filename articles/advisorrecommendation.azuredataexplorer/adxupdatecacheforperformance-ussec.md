<properties
    pageTitle="Reduce cache in Azure Data Explorer table"
    description="Reduce cache in Azure Data Explorer table"
    authors="lizlotor"
    ms.author="kustosee"
    articleId="389653ce-d564-4b95-aac4-ca30e1602536_USSec"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USSec"
    ownershipId="AzureDataExplorer_Kusto"
/>
# The following Azure Data Explorer tables have been identified as candidates for updating their cache settings
---
{
  "recommendationOfferingId": "0b85c950-0437-4844-be0e-dbbeced43ae5",
  "recommendationOfferingName": "Azure Data Explorer",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "389653ce-d564-4b95-aac4-ca30e1602536",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://kustodataestate.usseceast.kusto.core.microsoft.scloud').database('AdvisorRecommendations').PublishUpdateCacheForPerformanceRecommendations",
    "dataSource": "Kusto",
    "refreshInterval": "0.08:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Kusto/Clusters",
  "recommendationFriendlyName": "ReduceCacheForAzureDataExplorerTablesToImprovePerformance",
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
  "version": 1.8,
  "learnMoreLink": "https://aka.ms/adxcachepolicy",
  "description": "(PREVIEW) Reduce Azure Data Explorer table cache-period (policy) for better performance",
  "longDescription": "Reducing the table cache policy will free up unused data from Azure Data Explorer cluster's cache and will improve performance",
  "potentialBenefits": "Optimize performance",
  "actions": [
    {
      "actionId": "B2F98EEC-E41A-44E2-8B80-1AB27EAC8B3B",
      "description": "Update cache settings",
      "actionType": "ContextBlade",
	    "extensionName": "Microsoft_Azure_Kusto",
      "bladeName": "DatabaseOverviewBladeViewModel",
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
      "actionId": "7f859d48-5fd0-4431-8ffe-06783d10c647",
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