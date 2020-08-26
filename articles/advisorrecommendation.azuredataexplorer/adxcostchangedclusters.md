<properties
    pageTitle="Right-size cost Azure Data Explorer clusters."
    description="Right-size cost Azure Data Explorer clusters."
    authors="raldaba"
    ms.author="aoaft"
    articleId="567187Ba-1bdd-4dd8-ab70-6d494190df58_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="AzureOptimizationAutomation_AORec"
/>
# The following ADX clusters have been identified as candidates for re-scaling
---
{
  "recommendationOfferingId": "30e759db-a347-421d-a0b4-93a2ac30c1f8",
  "recommendationOfferingName": "Azure Data Explorer",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "4e13bb59-a859-45b5-ab5a-19363a34084e",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "cluster('https://cerebro.centralus.kusto.windows.net').database('CustomerPublish').AzureAdvisor_ADX_CostChangedReco",
    "dataSource": "Kusto",
    "refreshInterval": "0.04:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Kusto/clusters",
  "recommendationFriendlyName": "Right-size Azure Data Explorer clusters for cost",
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
    "serviceTreeId": "a3db6cf3-640c-4340-8381-108d31853b7f"
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
  "description": "(PREVIEW) Right-size Azure Data Explorer clusters for optimal cost",
  "longDescription": "(PREVIEW) This recommendation surfaces all Azure Data Explorer clusters which have low data capacity and CPU utilization. The recommended action to improve the cluster's performance is to scale down and/or scale in to the recommended cluster configuration shown.",
  "potentialBenefits": "Optimize cost",
  "actions": [
    {
      "actionId": "9bdcbfa6-0dbf-4c48-9291-587251102c63",
      "description": "Change your SKU to scale down",
      "actionType": "Blade",
	  "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}",
		"menuid": "scale_up"
      }
    },
	{
      "actionId": "10c9bd8e-e88e-4e42-b1cd-069fa043857e",
      "description": "Change your instance count to scale in",
      "actionType": "Blade",
	  "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}",
		"menuid": "scale_out"
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
  ],
  "costSavingInfo": "*You can save up to the stated amount if you choose to scale down your SKU or scale in your instances. Your actual savings may vary."
}
---
