<properties
    pageTitle="Consider increasing the size of your VNet Gateway SKU to address high P2S connection count"
    description="Consider increasing the size of your VNet Gateway SKU to address high P2S connection count"
    authors="raashman"
    ms.author="raashman"
    articleId="f78c8e26-9c40-4a74-a091-f76aecb49099_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="CloudNet_AzureVPNGateway"
/>
# Consider increasing the size of your VNet Gateway SKU to address high P2S use
---
{
  "recommendationOfferingId": "658a4a19-9c40-472b-a918-3f550848421a",
  "recommendationOfferingName": "VPN Gateway",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "f78c8e26-9c40-4a74-a091-f76aecb49099",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://azurecxpcre.kusto.windows.net').database('CXPCREGeneral').p2shighconnectioncountfairfax",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Network/virtualNetworkGateways",
  "recommendationFriendlyName": "HighP2SConnectionsVNetGateway",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "raashman@microsoft.com",
    "icm": {
      "routingId": "d8d41d18-4086-431a-b509-04f2d2ed6526",
      "service": "Windows Azure Operations Center",
      "team": "Azure CXP Crisis Escalation Management"
    },
    "serviceTreeId": "d8d41d18-4086-431a-b509-04f2d2ed6526"
  },
  "ingestionClientIdentities": [],
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/HighP2SConnectionsVNetGateway",
  "description": "Consider increasing the size of your VNet Gateway SKU to address high P2S use",
  "longDescription": "Each gateway SKU can only support a specified count of concurrent P2S connections. Your connection count is close to your gateway limit, so additional connection attempts may fail.",
  "potentialBenefits": "Increasing the size of your gateway will allow you to support more concurrent P2S users",
  "actions": [
    {
      "actionId": "9ac9a68c-7da7-48aa-85c5-54efd4e910a7",
      "description": "Consider scaling up your VNet Gateway",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}",
        "menuid": "configuration"
      },
      "documentLink": ""
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "9ac9a68c-7da7-48aa-85c5-54efd4e910a7",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      },
      "documentLink": ""
    }
  },
  "displayLabel": "P2S Gateway with High Connection Count",
  "additionalColumns": [{ "name": "HighestP2SPercentUtilized", "title": "% of Maximum" }],
  "tip": "",
  "costSavingInfo": "",
  "testData": "b93ce672-a2a1-44dc-bee9-86554fc186e7,/subscriptions/b93ce672-a2a1-44dc-bee9-86554fc186e7/resourceGroups/rgGW/providers/Microsoft.Network/virtualNetworkGateways/AzGovTestGW,{\"HighestP2SPercentUtilized\" : \"94.5\"}"
  }
---