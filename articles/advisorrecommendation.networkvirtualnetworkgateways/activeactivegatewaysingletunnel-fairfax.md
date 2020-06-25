<properties
    pageTitle="Configure redundant tunnel for your active-active VPN gateway"
    description="Configure redundant tunnel for your active-active VPN gateway"
    authors="anzaman"
    ms.author="alzam"
    articleId="f3be5a9b-2583-4a1c-b774-2481c00ccb04_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Configure redundant tunnel for your active-active VPN gateway
<!--issueDescription-->
---
{
  "recommendationOfferingId": "658a4a19-9c40-472b-a918-3f550848421a",
  "recommendationOfferingName": "VPN Gateway",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "f3be5a9b-2583-4a1c-b774-2481c00ccb04",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "cluster('https://aznwff.kusto.usgovcloudapi.net').database('aznwcosmos').FairfaxAAgateway1tunnel",
    "dataSource": "Kusto",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Network/virtualNetworkGateways",
  "recommendationFriendlyName": "ActiveActiveGatewaySingleTunnel",
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
  "version": 2.0,
  "learnMoreLink": "https://aka.ms/aa_activeactive_singletun_learnmore",
  "description": "Configure redundant tunnel for your active-active VPN gateway",
  "longDescription": "In active-active configuration, each Azure gateway instance has a unique public IP address, and each establishes an IPsec/IKE S2S VPN tunnel to your on-premises VPN device specified in your local network gateway and connection. Note that both VPN tunnels are actually part of the same connection. You need to configure your on-premises VPN device to accept or establish two S2S VPN tunnels to those two Azure VPN gateway public IP addresses.",
  "potentialBenefits": "Improve availability and aggregate throughput",
  "actions": [
    {
      "actionId": "1c8c2ec0-ad36-4c8e-acc5-29ca43e7ab24",
      "description": "Configure redundant tunnel",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aa_activeactive_singletun_learnmore"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "d0ae600c-2a83-4274-88ef-c7cbbd79c6cc",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Configure redundant tunnel",
  "additionalColumns": [],
  "tip": "You can configure redundant tunnels for your active-active vpn gateway to improve availability."
}
---
