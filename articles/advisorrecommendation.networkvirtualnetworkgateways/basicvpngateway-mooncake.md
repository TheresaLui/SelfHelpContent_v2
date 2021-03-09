<properties
    pageTitle="Move to production gateway SKUs from Basic gateways"
    description="Move to production gateway SKUs from Basic gateways"
    authors="anzaman"
    ms.author="alzam"
    articleId="e070c4bf-afaf-413e-bc00-e476b89c5f3d_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Move to production gateway SKUs from Basic gateways
---
{
  "recommendationOfferingId": "658a4a19-9c40-472b-a918-3f550848421a",
  "recommendationOfferingName": "VPN Gateway",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "e070c4bf-afaf-413e-bc00-e476b89c5f3d",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace":  "cluster('https://aznwchinamc.chinanorth2.kusto.chinacloudapi.cn').database('aznwmds').McBasicGateways",
    "dataSource": "Kusto",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Network/virtualNetworkGateways",
  "recommendationFriendlyName": "BasicVPNGateway",
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
  "learnMoreLink": "https://aka.ms/aa_basicvpngateway_learnmore",
  "description": "Move to production gateway SKUs from Basic gateways",
  "longDescription": "The VPN gateway Basic SKU is designed for development or testing scenarios. Please move to a production SKU if you are using the VPN gateway for production purposes. The production SKUs offer higher number of tunnels, BGP support, active-active, custom IPsec/IKE policy in addition to higher stability and availability.",
  "potentialBenefits": "Additional available features and higher stability and availability",
  "actions": [
    {
      "actionId": "303d98e9-f118-4849-9568-7aa3ef712f6b",
      "description": "Move away from the Basic VPN gateway SKU",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aa_basicvpngateway_action1"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "39668abb-3914-4fca-8904-6d843c109b09",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Move to production gateway SKUs from Basic gateways",
  "additionalColumns": []
}
---
