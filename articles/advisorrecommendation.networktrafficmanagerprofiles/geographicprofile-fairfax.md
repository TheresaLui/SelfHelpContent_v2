<properties
    pageTitle='Add an endpoint configured to "All (World)"'
    description='Add an endpoint configured to "All (World)"'
    authors="mattmccreesh"
    ms.author="mamccree"
    articleId="0bbe0a49-3c63-49d3-ab4a-aa24198f03f7_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    productPesIds="15400"
    cloudEnvironments="Fairfax"
    ownershipId="CloudNet_TrafficManager"
/>
# Add an endpoint configured to "All (World)"
---
{
  "recommendationOfferingId": "9264a786-286a-41e2-b8aa-4210461010a4",
  "recommendationOfferingName": "Traffic Manager",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "0bbe0a49-3c63-49d3-ab4a-aa24198f03f7",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "Fairfax.Production.Watm.Advisor.GeoEndpoints",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Network/trafficmanagerprofiles",
  "recommendationFriendlyName": "GeographicProfile",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "atmredmond@microsoft.com",
    "icm": {
      "routingId": "Metrics://TrafficManager",
      "service": "Cloudnet",
      "team": "TrafficManager"
    },
    "serviceTreeId": "d99081c1-c81f-49e3-8aec-541f00ffba62"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/Rf7vc5",
  "description": "Add an endpoint configured to \"All (World)\"",
  "longDescription": "For geographic routing, traffic is routed to endpoints based on defined regions. When a region fails, there is no pre-defined failover. Having an endpoint where the Regional Grouping is configured to \"All (World)\" for geographic profiles will avoid traffic black holing and guarantee service remains available.",
  "potentialBenefits": "Improve resiliency by avoiding traffic black holes",
  "actions": [
    {
      "actionId": "6d1e3db1-3e76-4e9a-acc0-26fa81688030",
      "description": "Add an \"All (World)\" endpoint",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}",
        "menuid": "endpoints"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "98cb0db6-eef6-48b3-acec-d05cf2f24de3",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Add Endpoint",
  "additionalColumns": []
}
---
