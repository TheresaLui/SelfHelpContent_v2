<properties
    pageTitle="Repurpose or delete idle virtual network gateways"
    description="Repurpose or delete idle virtual network gateways"
    authors="anzaman"
    ms.author="alzam"
    articleId="129d8c1e-a4d2-4bac-86ce-c7c2b2e37feb_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Repurpose or delete idle virtual network gateways
---
{
  "recommendationOfferingId": "658a4a19-9c40-472b-a918-3f550848421a",
  "recommendationOfferingName": "VPN Gateway",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "129d8c1e-a4d2-4bac-86ce-c7c2b2e37feb",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "cluster('https://aznwff.kusto.usgovcloudapi.net').database('aznwcosmos').FairfaxIdleGateways",
    "dataSource": "Kusto",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Network/virtualNetworkGateways",
  "recommendationFriendlyName": "IdleVNetGateway",
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
  "learnMoreLink": "https://aka.ms/aa_idlevpngateway_learnmore",
  "description": "Repurpose or delete idle virtual network gateways",
  "longDescription": "We noticed that your virtual network gateway has been idle for over 90 days. This gateway is being billed hourly. You may want to reconfigure this gateway, or delete it if you do not intend to use it any more.",
  "potentialBenefits": "savings",
  "actions": [
    {
      "actionId": "1864c21d-f32f-41df-b06f-dd9b7e0c7399",
      "description": "Delete or reconfigure the virtual network gateway",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Network",
      "bladeName": "VirtualNetworkGatewayBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "249727a2-ae2a-43eb-8cc2-2815e85c103d",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Network",
      "bladeName": "VirtualNetworkGatewayBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Delete or reconfigure idle virtual network gateways",
  "additionalColumns": [],
  "tip": "You can delete or repurpose idle virtual network gateways to reduce your Azure spend.",
  "costSavingInfo": "*You can save up to the stated amount if you choose to delete the virtual network gateway. Your actual savings may vary."
}
---
