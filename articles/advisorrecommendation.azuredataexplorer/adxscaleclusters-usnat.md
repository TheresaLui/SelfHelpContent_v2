<properties
    pageTitle="Right-size Azure Data Explorer (ADX) clusters."
    description="Right-size Azure Data Explorer (ADX) clusters."
    authors="prvavill"
    ms.author="kustosee"
    articleId="BD8A9EBF-E71A-4D65-A22B-7557917F2280_USNat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USNat"
    ownershipId="AzureDataExplorer_Kusto"
/>
# The following ADX clusters have been identified as candidates for re-scaling
---
{
  "recommendationOfferingId": "f69180f4-2eea-4124-a08d-c8ab3663a249",
  "recommendationOfferingName": "Azure Data Explorer",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "da4d47d5-b48b-4308-93bc-29d954424e76",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "cluster('https://kustodataestate.usnatwest.kusto.core.eaglex.ic.gov').database('AdvisorRecommendations').PublishPerformanceSkuChangeRecommendations",
    "dataSource": "Kusto",
    "refreshInterval": "0.08:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Kusto/clusters",
  "recommendationFriendlyName": "Right-size ADX cluster",
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
  "version": 2.0,
  "learnMoreLink": "https://azure.microsoft.com/pricing/details/data-explorer/",
  "description": "(PREVIEW) Right-size Azure Data Explorer clusters for optimal performance",
  "longDescription": "(PREVIEW) This recommendation surfaces all Azure Data Explorer clusters which exceed the recommended data capacity (80%). The recommended action to improve the cluster's performance is to scale to the recommended cluster configuration shown.",
  "potentialBenefits": "Optimize performance",
  "actions": [
    {
      "actionId": "40466365-EBF0-42A3-84A3-4F9A22BF019C",
      "description": "Resize the Cluster",
      "actionType": "ContextBlade",
      "extensionName": "Microsoft_Azure_Kusto",
      "bladeName": "SkuRecommendationBlade",
      "metadata": {
        "resource": "{resourceId}",
        "skuRecommendation": {
            "skuName": "{recommendedSku}",
            "isDevSku": "{isDevSku}",
            "instancesCount": "{recommendedInstanceCount}"
        },
        "description": "{description}",
        "recommendedConfig": "{recommendedConfig}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "2fad54ad-2907-4a6a-b5c2-180c726fa3e4",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Consider scaling your cluster to the recommended configuration",
  "additionalColumns": [
    {
      "name": "clusterName",
      "title": "Cluster Name"
    },
    {
      "name": "currentConfig",
      "title": "Current Configuration"
    },
    {
      "name": "recommendedConfig",
      "title": "Recommended Configuration"
    },
    {
      "name": "observationStartTime",
      "title": "Observation Start Time"
    },
    {
      "name": "observationEndTime",
      "title": "Observation End Time"
    }
  ]
}
---
