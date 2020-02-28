<properties
    pageTitle="Configure DNS Time to Live to 20 seconds"
    description="Configure DNS Time to Live to 20 seconds"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="b020ff96-37bf-4a64-8bd5-2bfb3fdf3f87_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
	ownershipId="CloudNet_TrafficManager"
/>
# Configure DNS Time to Live to 20 seconds
---
{
  "recommendationOfferingId": "9264a786-286a-41e2-b8aa-4210461010a4",
  "recommendationOfferingName": "Traffic Manager",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "b020ff96-37bf-4a64-8bd5-2bfb3fdf3f87",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "Public.Production.Watm.Advisor.FastFailoverTTL",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Network/trafficmanagerprofiles",
  "recommendationFriendlyName": "FastFailOverTTL",
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
  "learnMoreLink": "https://aka.ms/Ngfw4r",
  "description": "Configure DNS Time to Live to 20 seconds",
  "longDescription": "Time to Live (TTL) affects how recent of a response a client will get when it makes a request to Azure Traffic Manager. Reducing the TTL value means that the client will be routed to a functioning endpoint faster in the case of a failover. Configure your TTL to 20 seconds to route traffic to a health endpoint as quickly as possible.",
  "potentialBenefits": "Improve availability by failing over to healthy endpoints",
  "actions": [
    {
      "actionId": "5752f97c-1607-45ee-807b-4b003af71452",
      "description": "Configure your fast failover profile TTL to 20 seconds",
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
      "actionId": "5e6564b8-fb81-44e3-a0e2-abddf5a89923",
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
