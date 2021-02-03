<properties
    pageTitle="Detect unused or empty Azure Data Explorer (ADX) clusters."
    description="Detect unused or empty Azure Data Explorer (ADX) clusters."
    authors="prvavill"
    ms.author="kustosee"
    articleId="6DAFD3AF-0F4A-4F3B-AF9C-E85A2DD1FF8B_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="AzureDataExplorer_Kusto"
/>
# The following ADX clusters are not being used and are candidates for deletion.
---
{
  "recommendationOfferingId": "f69180f4-2eea-4124-a08d-c8ab3663a249",
  "recommendationOfferingName": "Azure Data Explorer",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "d9c2f871-904e-4907-8572-0a33b0651f01",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "cluster('https://kustodataestate.chinaeast2.kusto.chinacloudapi.cn').database('AdvisorRecommendations').PublishUnusedClustersRecommendations",
    "dataSource": "Kusto",
    "refreshInterval": "0.08:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Kusto/clusters",
  "recommendationFriendlyName": "ADX Unused cluster",
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
  "learnMoreLink": "https://www.azure.cn/pricing/details/data-explorer/",
  "description": "(PREVIEW) Unused/Empty Azure Data Explorer clusters",
  "longDescription": "(PREVIEW) This recommendation surfaces all Azure Data Explorer clusters which were provisioned more than 10 days ago from this recommendation generated date and found either completely empty or with no activity. The recommended action is to validate and consider deleting the empty or unused Azure Data Explorer clusters.",
  "potentialBenefits": "Optimize Azure spend",
  "actions": [
    {
      "actionId": "2f150ed8-58b6-485c-9843-2efac1d74e35",
      "description": "Consider deleting empty or unused clusters",
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
      "actionId": "2fad54ad-2907-4a6a-b5c2-180c726fa3e4",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Consider deleting empty or unused clusters",
  "additionalColumns": [
    {
      "name": "instanceCount",
      "title": "Instance Count"
    },
    {
      "name": "region",
      "title": "Region"
    },
    {
      "name": "vmSku",
      "title": "VM SKU"
    },
    {
      "name": "recGeneratedOn",
      "title": "Generated On"
    }
  ],
  "costSavingInfo": "Cost savings are estimated for a year in USD"
}
---
