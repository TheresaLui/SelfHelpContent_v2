<properties
    pageTitle="Right-size Azure Data Explorer clusters."
    description="Right-size Azure Data Explorer clusters."
    authors="raldaba"
    ms.author="aoaft"
    articleId="53c3a9f6-baa8-4997-b5a5-a3b5d3347afe_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureDataExplorer_Kusto"
/>
# The following ADX clusters have been identified as candidates for re-scaling
---
{
  "recommendationOfferingId": "d09be8a5-3108-430b-9182-25441e2025e7",
  "recommendationOfferingName": "Azure Data Explorer",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "da4d47d5-b48b-4308-93bc-29d954424e76",
  "dataSourceMetadata": {
    "schemaVersion": 2.1,
    "streamNamespace": "cluster('https://cerebro.centralus.kusto.windows.net').database('CustomerPublish').AzureAdvisor_ADX_ScaleClusterReco",
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
    "email": "aoaft@microsoft.com",
    "icm": {
      "routingId": "AORECOMMENDATIONS\\Triage",
      "service": "AO Recommendations",
      "team": "Triage"
    },
    "serviceTreeId": "a3db6cf3-640c-4340-8381-108d31853b7f"
  },
  "ingestionClientIdentities": [
    "6c75c76c-7792-4dd0-8e85-ad598f14bc93",
    "db97364d-48bf-4567-af34-e0843d0ee0af",
    "bd26e40e-c0cc-4d1d-8801-569dac0cd7fe",
    "9c14bff5-1bda-4de6-a74f-4c3caa370570"
  ],
  "recommendationTimeToLive": 86400,
  "version": 3.0,
  "learnMoreLink": "https://aka.ms/adxskuperformance",
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
            "isDevSku": {isDevSku},
            "instancesCount": {recommendedInstanceCount}
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
  ],
  "testData": "a0cd6542-7eaf-43d2-bbdd-b678a869aad1,/subscriptions/a0cd6542-7eaf-43d2-bbdd-b678a869aad1/resourceGroups/demostggroup/providers/Microsoft.Kusto/Clusters/demov3"
}
---
