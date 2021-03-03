<properties
    pageTitle="Right-size cost Azure Data Explorer clusters."
    description="Right-size cost Azure Data Explorer clusters."
    authors="raldaba"
    ms.author="aoaft"
    articleId="567187Ba-1bdd-4dd8-ab70-6d494190df58_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureDataExplorer_Kusto"
/>
# The following ADX clusters have been identified as candidates for re-scaling
---
{
  "recommendationOfferingId": "30e759db-a347-421d-a0b4-93a2ac30c1f8",
  "recommendationOfferingName": "Azure Data Explorer",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "4e13bb59-a859-45b5-ab5a-19363a34084e",
  "dataSourceMetadata": {
    "schemaVersion": 2.1,
    "streamNamespace": "cluster('https://cerebro.centralus.kusto.windows.net').database('CustomerPublish').AzureAdvisor_ADX_CostChangedReco",
    "dataSource": "Kusto",
    "refreshInterval": "0.08:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Kusto/clusters",
  "recommendationFriendlyName": "Right-size ADX clusters for cost",
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
  "learnMoreLink": "https://aka.ms/adxskusize",
  "description": "(PREVIEW) Right-size Azure Data Explorer clusters for optimal cost",
  "longDescription": "(PREVIEW) This recommendation surfaces all Azure Data Explorer clusters which have low data capacity and CPU utilization. The recommended action to improve the cluster's performance is to scale down and/or scale in to the recommended cluster configuration shown.",
  "potentialBenefits": "Optimize cost",
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
      "actionId": "216d3260-6c8c-4d41-93b4-702605a3a7e8",
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
  "costSavingInfo": "*Your actual yearly savings may vary. The yearly saving that is presented is based on 'pay as you go' prices. The potential saving does not take into consideration Azure Reserved VM Instances (RIs) billing discounts you may have."
}
---
