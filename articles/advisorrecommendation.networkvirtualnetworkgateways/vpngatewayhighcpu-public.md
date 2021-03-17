<properties
    pageTitle="Consider increasing the size of your VNet Gateway SKU to address high CPU"
    description="Consider increasing the size of your VNet Gateway SKU to address high CPU"
    authors="evanba"
    ms.author="evanba"
    articleId="2e41fe84-7173-4fe9-b257-61aa4679c3fe_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="CloudNet_AzureVPNGateway"
/>
# Consider increasing the size of your VNet Gateway SKU to address high CPU
---
{
  "recommendationOfferingId": "658a4a19-9c40-472b-a918-3f550848421a",
  "recommendationOfferingName": "VPN Gateway",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "2e41fe84-7173-4fe9-b257-61aa4679c3fe",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://azurecxpcre.kusto.windows.net').database('CXPCREGeneral').NVAHighCPU",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Network/virtualNetworkGateways",
  "recommendationFriendlyName": "HighCPUVNetGateway",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "evanba@microsoft.com",
    "icm": {
      "routingId": "d8d41d18-4086-431a-b509-04f2d2ed6526",
      "service": "Windows Azure Operations Center",
      "team": "Azure CXP Crisis Escalation Management"
    },
    "serviceTreeId": "d8d41d18-4086-431a-b509-04f2d2ed6526"
  },
  "ingestionClientIdentities": [],
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/HighCPUP2SVNetGateway",
  "description": "Consider increasing the size of your VNet Gateway SKU to address consistently high CPU use",
  "longDescription": "Under high traffic load, the VPN gateway may drop packets due to high CPU. You should consider upgrading your VPN Gateway SKU since your VPN has consistently been running at .",
  "potentialBenefits": "Increasing the size of your VPN gateway will ensure that connections aren't dropped due to high CPU",
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
  "displayLabel": "VPN Gateway with High CPU",
  "additionalColumns": [],
  "tip": "",
  "costSavingInfo": "",
  "testData": "27b2ee0a-4093-4253-95b5-c595487ad66f,/subscriptions/27b2ee0a-4093-4253-95b5-c595487ad66f/resourceGroups/rgGW/providers/Microsoft.Network/virtualNetworkGateways/testGW"
  }
---
