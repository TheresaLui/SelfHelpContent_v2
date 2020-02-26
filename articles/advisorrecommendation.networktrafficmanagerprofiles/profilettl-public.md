<properties
    pageTitle="Configure DNS Time to Live to 60 seconds"
    description="Configure DNS Time to Live to 60 seconds"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="d374a732-e69b-41dc-bbc2-a7234e2270be_Public"
    selfHelpType="advisorRecommendationMetadata"
    productPesIds="15400"
    cloudEnvironments="Public"
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
    "streamNamespace": "Public.Production.Watm.Advisor.ProfileTTL",
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
    "email": "aadevteam@microsoft.com",
    "icm": {
      "routingId": "MDM://AzureAdvisor",
      "service": "Azure Advisor",
      "team": "Azure Advisor"
    },
    "serviceTreeId": "f6d7f416-ee14-4943-894b-1abca9140b74"
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
      "extensionName": "Microsoft_Azure_Network",
      "bladeName": "TrafficManagerBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Configure Time to Live",
  "additionalColumns": []
}
---
