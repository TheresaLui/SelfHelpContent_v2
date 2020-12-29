<properties
    pageTitle="Review application gateways that are running hot to see if they need to be scaled more"
    description="Review application gateways that are running hot to see if they need to be scaled more"
    ms.author="evanba"
    articleId="2ee9f31e-df58-4893-b3e7-66c0cd74183a"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
    ownershipId="CloudNet_AzureApplicationGateway"
/>
# Increase your instance count for gateways running hot
---
{
  "recommendationOfferingId": "dd4296e3-3037-49b2-a443-1f17d54a0720",
  "recommendationOfferingName": "Hot Application Gateway",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "2ee9f31e-df58-4893-b3e7-66c0cd74183a",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://AzureCXPCRE.kusto.windows.net').database('CXPCREMaint').FindHotAppGWs",
    "dataSource": "Kusto",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Network/applicationGateways",
  "recommendationFriendlyName": "HotAppGateway",
  "recommendationMetadataState": "",
    "email": "appgwpm@microsoft.com",
    "icm": {
      "routingId": "adrocs://Recovery/AppGWT",
      "service": "Azure Application Gateway",
      "team": "Azure Application Gateway"
    },
    "serviceTreeId": "95028b6a-341d-461d-bffd-f83b7eddf59f"
  },
  "ingestionClientIdentities": [],
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/hotappgw",
  "description": "Make sure you have your Application Gateway configured for enough instances to support the traffic",
  "longDescription": "When under high load, Application Gateways can drop traffic. In order to prevent that, make sure you have enough instances to sufficiently spread the traffic out across the instances. For v1 (Standard/WAF), you need to specify a high enough instance count while for v2 (Standard_v2/WAF_v2), you need to enable autoscaling a properly set the minimum and maximum instance counts",
  "potentialBenefits": "Ensure availability of your sites",
  "actions": [
    {
      "actionId": "9f4bbd2d-c3cf-4c9b-8e15-e6ae661ea291",
      "description": "Blade",
      "actionType": "HubsExtension",
      "extensionName": "ResourceMenuBlade",
      "bladeName": "",
      "metadata": {
        "id":"{resourceId}",
        "menuid": "Configuration"
      },
      "documentLink": ""
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "9f4bbd2d-c3cf-4c9b-8e15-e6ae661ea291",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id":"{resourceId}"
      },
      "documentLink": ""
    }
  },
  "displayLabel": "Properly scale your Application Gateway",
  "additionalColumns": [],
  "tip": "Properly scale your Application Gateway",
  "costSavingInfo": "",
  "testData":
    "27b2ee0a-4093-4253-95b5-c595487ad66f,/subscriptions/27b2ee0a-4093-4253-95b5-c595487ad66f/resourceGroups/rgHotAppGW/providers/Microsoft.Network/applicationGateways/v2_testhot",
    "27b2ee0a-4093-4253-95b5-c595487ad66f,/subscriptions/27b2ee0a-4093-4253-95b5-c595487ad66f/resourceGroups/rgHotAppGW/providers/Microsoft.Network/applicationGateways/v1test"
}
---
