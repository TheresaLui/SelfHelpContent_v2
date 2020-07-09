<properties
    pageTitle="Configure DNS Time to Live to 60 seconds"
    description="Configure DNS Time to Live to 60 seconds"
    authors="mattmccreesh"
    ms.author="mamccree"
    articleId="d374a732-e69b-41dc-bbc2-a7234e2270be_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    productPesIds="15400"
    cloudEnvironments="Fairfax"
    ownershipId="CloudNet_TrafficManager"
/>
# Configure DNS Time to Live to 60 seconds
---
{
  "recommendationOfferingId": "9264a786-286a-41e2-b8aa-4210461010a4",
  "recommendationOfferingName": "Traffic Manager",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "d374a732-e69b-41dc-bbc2-a7234e2270be",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "Fairfax.Production.Watm.Advisor.ProfileTTL",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Network/trafficmanagerprofiles",
  "recommendationFriendlyName": "ProfileTTL",
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
  "learnMoreLink": "https://aka.ms/Um3xr5",
  "description": "Configure DNS Time to Live to 60 seconds",
  "longDescription": "Time to Live (TTL) affects how recent of a response a client will get when it makes a request to Azure Traffic Manager. Reducing the TTL value means that the client will be routed to a functioning endpoint faster in the case of a failover. Configure your TTL to 60 seconds to route traffic to a health endpoint as quickly as possible.",
  "potentialBenefits": "Improve availability by failing over to healthy endpoints faster",
  "actions": [
    {
      "actionId": "151f3e91-ccff-44b9-8e5c-6f8c4f796319",
      "description": "Configure your profile TTL to 60 seconds",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}",
        "menuid": "configuration"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "75b83538-dfc6-4da9-94c1-9fc79fd3ebdb",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Configure Time to Live",
  "additionalColumns": []
}
---
