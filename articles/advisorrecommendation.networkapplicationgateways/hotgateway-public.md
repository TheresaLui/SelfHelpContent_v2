<properties
    pageTitle="Review application gateways that are running hot to see if they need to be scaled more"
    description="Review application gateways that are running hot to see if they need to be scaled more"
    ms.author="evanba"
    articleId="2ee9f31e-df58-4893-b3e7-66c0cd74183a_Public"
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
    "refreshInterval": "00.01:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Network/applicationGateways",
  "recommendationFriendlyName": "HotAppGateway",
  "recommendationMetadataState": "Active",
  "owner": {
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
  "description": "Make sure you have enough instances in your Application Gateway to support your traffic",
  "longDescription": "Your Application Gateway has been running on high utilization recently and under heavy load, you may experience traffic loss or increase in latency. It is important that you scale your Application Gateway according to your traffic and with a bit of a buffer so that you are prepared for any traffic surges or spikes and minimizing the impact that it may have in your QoS. Application Gateway v1 SKU (Standard/WAF) supports manual scaling and v2 SKU (Standard_v2/WAF_v2) support manual and autoscaling. In case of manual scaling, increase your instance count and if autoscaling is enabled, make sure your maximum instance count is set to a higher value so Application Gateway can scale out as the traffic increases",
  "potentialBenefits": "Ensure availability of your sites",
  "actions": [
    {
      "actionId": "9f4bbd2d-c3cf-4c9b-8e15-e6ae661ea291",
      "description": "Inspect your Application Gateway scaling configuration",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Network",
      "bladeName": "ApplicationGatewayConfigurationBlade",
      "metadata": {
        "id":"{resourceId}"
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
        "id":"{resourceId}",
        "menuid": "configuration"
      },
      "documentLink": ""
    }
  },
  "displayLabel": "Properly scale your Application Gateway",
  "additionalColumns": [
    {
    "name": "DeltaHitCountFromPrevious",
    "title": "Count of Exceeding CPU Limit"
    },
    {"name": "DeltaMinCountFromPrevious",
    "title": "Timespan"
    }
  ],
  "tip": "Properly scale your Application Gateway",
  "costSavingInfo": "",
  "testData": "27b2ee0a-4093-4253-95b5-c595487ad66f,/subscriptions/27b2ee0a-4093-4253-95b5-c595487ad66f/resourceGroups/rgHotAppGW/providers/Microsoft.Network/applicationGateways/v2_testhot, \"{\"\"DeltaHitCountFromPrevious\"\" : \"\"8\"\", \"\"DeltaMinCountFromPrevious\"\" : \"\"Last 5 minutes\"\"}\""
}
---
