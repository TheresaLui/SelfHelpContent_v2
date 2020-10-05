<properties
    pageTitle="Right-size cost Azure Data Explorer (ADX) clusters."
    description="Right-size cost Azure Data Explorer (ADX) clusters."
    authors="prvavill"
    ms.author="kustosee"
    articleId="E3928E39-C27E-4DE2-8794-7157AAA94FE3_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="AzureDataExplorer_Kusto"
/>
# The following ADX clusters have been identified as candidates for re-scaling
---
{
  "recommendationOfferingId": "f69180f4-2eea-4124-a08d-c8ab3663a249",
  "recommendationOfferingName": "Azure Data Explorer",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "4e13bb59-a859-45b5-ab5a-19363a34084e",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "cluster('https://kustodataestate.chinaeast2.kusto.chinacloudapi.cn').database('AdvisorRecommendations').PublishCostSkuChangeRecommendations",
    "dataSource": "Kusto",
    "refreshInterval": "0.08:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Kusto/clusters",
  "recommendationFriendlyName": "Right-size ADX clusters for cost",
  "recommendationMetadataState": "Active",
  "recommendationScope": "Internal",
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
  "learnMoreLink": "https://www.azure.cn/pricing/details/data-explorer/",
  "description": "(PREVIEW) Right-size Azure Data Explorer clusters for optimal cost",
  "longDescription": "(PREVIEW) This recommendation surfaces all Azure Data Explorer clusters which have low data capacity and CPU utilization. The recommended action to improve the cluster's performance is to scale down and/or scale in  to the recommended cluster configuration shown.",
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
