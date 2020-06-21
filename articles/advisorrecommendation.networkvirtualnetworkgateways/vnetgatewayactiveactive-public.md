<properties
    pageTitle="Enable Active-Active gateways for redundancy"
    description="Enable Active-Active gateways for redundancy"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="c249dc0e-9a17-423e-838a-d72719e8c5dd_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Enable Active-Active gateways for redundancy
---
{
  "recommendationOfferingId": "658a4a19-9c40-472b-a918-3f550848421a",
  "recommendationOfferingName": "VPN Gateway",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "c249dc0e-9a17-423e-838a-d72719e8c5dd",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "Microsoft.Cloud.ActivePassiveVPNGatewaysAzureAdvisor",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Network/virtualNetworkGateways",
  "recommendationFriendlyName": "VNetGatewayActiveActive",
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
  "learnMoreLink": "https://aka.ms/aa_vpnha_learnmore",
  "description": "Enable Active-Active gateways for redundancy",
  "longDescription": "In active-active configuration, both instances of the VPN gateway will establish S2S VPN tunnels to your on-premise VPN device. When a planned maintenance or unplanned event happens to one gateway instance, traffic will be switched over to the other active IPsec tunnel automatically.",
  "potentialBenefits": "Ensure business continuity through connection resilience",
  "actions": [
    {
      "actionId": "e5477f4e-4bbd-4896-acf7-ea22f84939ec",
      "description": "Enable Active-Active gateways",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Network",
      "bladeName": "VirtualNetworkGatewayConfigurationBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "d10285d7-edee-448b-b621-1b35da898993",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Enable Active-Active gateways for redundancy",
  "additionalColumns": [],
  "tip": "Enable Active-Active configuration for your VPN gateways for redundancy."
}
---
