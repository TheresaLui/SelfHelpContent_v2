<properties
    pageTitle="Add or move one endpoint to another Azure region"
    description="Add or move one endpoint to another Azure region"
    authors="mattmccreesh"
    ms.author="mamccree"
    articleId="0db76759-6d22-4262-93f0-2f989ba2b58e_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    productPesIds="15400"
    cloudEnvironments="Fairfax"
    ownershipId="CloudNet_TrafficManager"
/>
# Add or move one endpoint to another Azure region
---
{
  "recommendationOfferingId": "9264a786-286a-41e2-b8aa-4210461010a4",
  "recommendationOfferingName": "Traffic Manager",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "0db76759-6d22-4262-93f0-2f989ba2b58e",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "Fairfax.Production.Watm.Advisor.PrEndpoints",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Network/trafficmanagerprofiles",
  "recommendationFriendlyName": "ProximityProfile",
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
  "learnMoreLink": "https://aka.ms/Ldkkdb",
  "description": "Add or move one endpoint to another Azure region",
  "longDescription": "All endpoints associated to this proximity profile are in the same region. Users from other regions may experience long latency when attempting to connect. Adding or moving an endpoint to another region will improve overall performance for proximity routing and provide better availability if all endpoints in one region fail.",
  "potentialBenefits": "Improve resiliency by allowing failover to another region",
  "actions": [
    {
      "actionId": "cd463052-0764-40c2-9f1b-99118d34825c",
      "description": "Add or move one endpoint to another Azure region",
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
      "actionId": "36168ba0-c0bc-4f9e-998e-9322ea48cc3a",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Add or Move Endpoint",
  "additionalColumns": []
}
---
