<properties
    pageTitle="Update cache policies in Azure Data Explorer table"
    description="Update cache policies for Azure Data Explorer tables"
    authors="raldaba"
    ms.author="aoaft"
    articleId="d437a3b5-c7a2-4162-83a2-ba8e7ce18d99_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureOptimizationAutomation_AORec"
/>
# The following Azure Data Explorer tables have been identified as candidates for updating their cache settings
---
{
  "recommendationOfferingId": "0b85c950-0437-4844-be0e-dbbeced43ae5",
  "recommendationOfferingName": "Azure Data Explorer",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "f011adf6-475a-48c9-bf26-8db051cb6964",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "cluster('https://cerebro.centralus.kusto.windows.net').database('CustomerPublish').AzureAdvisor_ADX_LimitQueryReco",
    "dataSource": "Kusto",
    "refreshInterval": "0.04:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Kusto/Clusters/Databases",
  "recommendationFriendlyName": "Update Cache Policies for ADX tables",
  "recommendationMetadataState": "Active",
  "recommendationScope": "Internal",
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
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/adxcachepolicy",
  "description": "(PREVIEW) Review Azure Data Explorer table cache-period (policy) for better performance",
  "longDescription": "This recommendation surfaces Azure Data Explorer tables which have a high number of queries that look back beyond the configured cache period (policy) (You will see the top 10 tables by query percentage that access out-of-cache data). The recommended action to improve the cluster's performance: Limit queries on this table to the minimal necessary time range (within the defined policy). Alternatively, if data from the entire time range is required, increase the cache period to the recommended value.",
  "potentialBenefits": "Optimize performance",
  "actions": [
    {
      "actionId": "d437a3b5-c7a2-4162-83a2-ba8e7ce18d99",
      "description": "Update cache period",
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
