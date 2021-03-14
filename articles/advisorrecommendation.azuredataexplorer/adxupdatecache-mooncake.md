<properties
    pageTitle="Reduce cache in Azure Data Explorer table"
    description="Reduce cache for Azure Data Explorer tables"
    authors="prvavill"
    ms.author="kustosee"
    articleId="79EB08B9-3448-4405-B0D9-1747BEEC2B89_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
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
    "streamNamespace": "cluster('https://kustodataestate.chinaeast2.kusto.chinacloudapi.cn').database('AdvisorRecommendations').PublishUnusedClustersRecommendations",
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
  "version": 4.1,
  "learnMoreLink": "https://docs.azure.cn/zh-cn/data-explorer/kusto/management/cachepolicy",
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
      "title": "Est. Data Savings"
    },
    {
      "name": "potentialInstancesSave",
      "title": "Potential Instances Save"
    },
	{
      "name": "requiredDataReductionForScaleIn",
      "title": "Req. Data Reduction for Scale-In"
    },
	{
      "name": "observationWindow",
      "title": "Observation Window"
    }
  ],
  "costSavingInfo": "*Your actual yearly savings may vary. The yearly saving that is presented is based on 'pay as you go' prices. The potential saving does not take into consideration Azure Reserved VM Instances (RIs) billing discounts you may have."
}
---
