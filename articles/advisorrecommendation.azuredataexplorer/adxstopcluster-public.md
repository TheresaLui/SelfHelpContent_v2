<properties
    pageTitle="Stop Azure Data Explorer clusters."
    description="Stop Azure Data Explorer clusters."
    authors="t-elbery"
    ms.author="kustosee"
    articleId="354D7BBB-A243-4BE1-A8B9-43DBFC05C44A_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureDataExplorer_Kusto"
/>
# The following ADX clusters have been identified as candidates for stopping.
---
{
  "recommendationOfferingId": "14AB98D0-DF29-43BE-B0EF-BB95432F0D40",
  "recommendationOfferingName": "Azure Data Explorer",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "354D7BBB-A243-4BE1-A8B9-43DBFC05C44A",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://kustodataestate.westeurope.kusto.windows.net').database('AdvisorRecommendations').PublishStoppedClustersRecommendations",
    "dataSource": "Kusto",
    "refreshInterval": "0.08:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Kusto/Clusters",
  "recommendationFriendlyName": "StopUnusedClustersWithData",
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
  "learnMoreLink": "http://aka.ms/adxunusedcluster",
  "description": "(PREVIEW) Unused Azure Data Explorer clusters with data",
  "longDescription": "(PREVIEW) This recommendation surfaces all Azure Data Explorer clusters which were provisioned more than 10 days ago from this recommendation generated date and found with no activity but containing data. The recommended action is to validate and consider stopping the unused Azure Data Explorer clusters.",
  "potentialBenefits": "Optimize Azure spend",
  "actions": [
    {
      "actionId": "2f150ed8-58b6-485c-9843-2efac1d74e35",
      "description": "Consider stopping unused clusters",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
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
  "displayLabel": "Consider stopping unused clusters",
  "additionalColumns": [
    {
      "name": "currentConfig",
      "title": "Current Configuration"
    },
    {
      "name": "region",
      "title": "Region"
    },
    {
      "name": "observationEndTime",
      "title": "Generated On"
    }
  ],
  "costSavingInfo": "Cost savings are estimated for a year in USD"
}
---