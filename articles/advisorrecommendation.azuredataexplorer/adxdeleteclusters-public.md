<properties
    pageTitle="Detect unused or empty Azure Data Explorer clusters."
    description="Detect unused or empty Azure Data Explorer clusters."
    authors="raldaba"
    ms.author="aoaft"
    articleId="d9c2f871-904e-4907-8572-0a33b0651f01_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="AzureDataExplorer_Kusto"
/>
# The following ADX clusters are not being used and are candidates for deletion.
---
{
  "recommendationOfferingId": "ee2562f9-b582-433a-9d20-1c8bdd53c199",
  "recommendationOfferingName": "Azure Data Explorer",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "d9c2f871-904e-4907-8572-0a33b0651f01",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://kustodataestate.westeurope.kusto.windows.net').database('AdvisorRecommendations').PublishUnusedClustersRecommendations",
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
  "learnMoreLink": "https://aka.ms/adxemptycluster",
  "description": "(PREVIEW) Unused/Empty Azure Data Explorer clusters",
  "longDescription": "(PREVIEW) This recommendation surfaces all Azure Data Explorer clusters which have a small amount of data, queries, and ingestions during the last 30 days; has low CPU usage during the last two days, and has no followers during the last day (the dates are from the recommendation generated date). The recommended action is to validate and consider deleting the empty or unused Azure Data Explorer clusters.",
  "potentialBenefits": "Optimize cost",
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
  "costSavingInfo": "*Your actual yearly savings may vary. The yearly saving that is presented is based on 'pay as you go' prices. The potential saving does not take into consideration Azure Reserved VM Instances (RIs) billing discounts you may have."
}
---
