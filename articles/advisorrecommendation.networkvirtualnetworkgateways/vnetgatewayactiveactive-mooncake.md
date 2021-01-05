<properties
    pageTitle="Enable Active-Active gateways for redundancy"
    description="Enable Active-Active gateways for redundancy"
    authors="anzaman"
    ms.author="alzam"
    articleId="c249dc0e-9a17-423e-838a-d72719e8c5dd_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Enable Active-Active gateways for redundancy
<!--issueDescription-->
---
{
  "recommendationOfferingId": "658a4a19-9c40-472b-a918-3f550848421a",
  "recommendationOfferingName": "VPN Gateway",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "c249dc0e-9a17-423e-838a-d72719e8c5dd",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "cluster('https://aznwchinamc.chinanorth2.kusto.chinacloudapi.cn').database('aznwmds').McActiveActiveGateways",
    "dataSource": "Kusto",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Network/virtualNetworkGateways",
  "recommendationFriendlyName": "VNetGatewayActiveActive",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "azvpnpms@microsoft.com",
    "icm": {
      "routingId": "MDM://vpngateway",
      "service": "VPN Gateway",
      "team": "VPN Gateway"
    },
    "serviceTreeId": "10c9bf14-f656-4413-a32c-176b6f203911"
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
