<properties
    pageTitle="Consider increasing the size of your VNet Gateway SKU to address high P2S connection count"
    description="Consider increasing the size of your VNet Gateway SKU to address high P2S connection count"
    authors="evanba"
    ms.author="evanba"
    articleId="f78c8e26-9c40-4a74-a091-f76aecb49099_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
    ownershipId=""
/>
# Consider increasing the size of your VNet Gateway SKU to address high P2S use
---
{
  "recommendationOfferingId": "658a4a19-9c40-472b-a918-3f550848421a",
  "recommendationOfferingName": "VPN Gateway",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "f78c8e26-9c40-4a74-a091-f76aecb49099",
  "dataSourceMetadata": {
    "streamNamespace": "",
    "dataSource": "",
    "refreshInterval": ""
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Network/virtualNetworkGateways",
  "recommendationFriendlyName": "HighP2SConnectionsVNetGateway",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "",
    "icm": {
      "routingId": "",
      "service": "",
      "team": ""
    },
    "serviceTreeId": ""
  },
  "ingestionClientIdentities": [],
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/HighP2SConnectionsVNetGateway",
  "description": Consider increasing the size of your VNet Gateway SKU to address high P2S use",
  "longDescription": "Each gateway SKU can only support a specified count of concurrent P2S connections. Your connection count is close to your gateway limit, so additional connection attempts may fail.",
  "potentialBenefits": "",
  "actions": [
    {
      "actionId": "9ac9a68c-7da7-48aa-85c5-54efd4e910a7",
      "description": "Scale up your VNet Gateway",
      "actionType": "Blade",
      "extensionName": "",
      "bladeName": "",
      "metadata": {},
      "documentLink": ""
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "",
      "actionType": "",
      "extensionName": "",
      "bladeName": "",
      "metadata": {},
      "documentLink": ""
    }
  },
  "displayLabel": "",
  "additionalColumns": [],
  "tip": "",
  "costSavingInfo": "",
  "testData": ""
}
---
