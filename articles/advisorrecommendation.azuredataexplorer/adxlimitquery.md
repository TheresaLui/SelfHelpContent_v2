<properties
    pageTitle="Increase cache performance in Azure Data Explorer (ADX) table"
    description="Increase cache performance for Azure Data Explorer (ADX) tables"
    authors="raldaba"
    ms.author="aoaft"
    articleId="d437a3b5-c7a2-4162-83a2-ba8e7ce18d99_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="AzureOptimizationAutomation_AORec"
/>
# The following ADX tables have been identified as candidates for updating their cache settings
---
{
  "recommendationOfferingId": "0b85c950-0437-4844-be0e-dbbeced43ae5",
  "recommendationOfferingName": "Azure Data Explorer",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "f011adf6-475a-48c9-bf26-8db051cb6964",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "cluster('https://cerebro.centralus.kusto.windows.net').database('Publish').AzureAdvisor_ADX_LimitQueryReco",
    "dataSource": "Kusto",
    "refreshInterval": "0.04:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Kusto/Clusters/Databases",
  "recommendationFriendlyName": "Increase cache performance for ADX tables",
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
  "learnMoreLink": "https://azure.microsoft.com/pricing/details/data-explorer/",
  "description": "(PREVIEW) Review ADX table cache to increase performance",
  "longDescription": "(PREVIEW) This recommendation surfaces all Azure Data Explorer clusters which have a high number of queries that look back beyond the configured cache settings. The recommended action to improve the cluster's performance is to limit the queries within the defined policy or increase the cache setting to the recommended value.",
  "potentialBenefits": "Optimize performance",
  "actions": [
    {
      "actionId": "d437a3b5-c7a2-4162-83a2-ba8e7ce18d99",
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
      "actionId": "f702dbb7-6a38-41ed-ab6e-1af313ad260e",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Consider setting your cache to the recommended value",
  "additionalColumns": [
	{
      "name": "tableName",
      "title": "Table Name"
    },
	{
      "name": "currentConfig",
      "title": "Current Config"
    },
	{
      "name": "cacheUsage",
      "title": "Current Usage"
    },
	{
      "name": "recommendedConfig",
      "title": "Recommended Config"
    },
	{
      "name": "observationWindow",
      "title": "Observation Window"
    }
  ]
}
---
