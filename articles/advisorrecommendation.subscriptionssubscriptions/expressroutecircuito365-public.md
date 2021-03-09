<properties
    pageTitle="Create additional ExpressRoute Circuits in another location for redundancy"
    description="Create additional ExpressRoute Circuits in another location for redundancy"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="3f000a35-4cf7-44ef-8127-2f7ed7909125_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="CloudNet_AzureExpressRoute"
/>
# Create additional ExpressRoute Circuits in another location for redundancy
---
{
  "recommendationOfferingId": "3e80411f-1930-4048-abf3-235c22b3850a",
  "recommendationOfferingName": "ExpressRoute",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "3f000a35-4cf7-44ef-8127-2f7ed7909125",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "AzureAnalytics.Partner.Networking.ExR.O365SingleERLocationAzureAdvisor_Pub",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Subscriptions/subscriptions",
  "recommendationFriendlyName": "ExpressRouteCircuitO365",
  "recommendationMetadataState": "Disabled",
  "portalFeatures": [],
  "owner": {
    "email": "ExRPM@microsoft.com",
    "icm": {
      "routingId": "AIMS://ExpressRoute",
      "service": "Cloudnet",
      "team": "ExpressRoute"
    },
    "serviceTreeId": "7269b88e-b638-4ba5-a55e-5632365dd938"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/o365ERAdvisor",
  "description": "Create additional ExpressRoute Circuits in another location for redundancy",
  "longDescription": "Customers using Microsoft Peering for Office 365 services should have at least two ExpressRoute Circuits in different locations to avoid a single point of failure. Create an additional ExpressRoute circuit to have a redundant connection in case of any failure.",
  "potentialBenefits": "Avoid a single point of failure",
  "actions": [
    {
      "actionId": "097540d4-33b4-4ea6-8e20-c2ac60ef108e",
      "description": "Create an additional ExpressRoute Circuit",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aa_exr_action"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "ac6cf7ad-8618-43bf-8c52-5befea409034",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Create additional ExpressRoute circuits",
  "additionalColumns": [],
  "tip": "You can avoid a single point of failure by creating an additional ExpressRoute circuit at a different location."
}
---
