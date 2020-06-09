<properties
    pageTitle="Consider increasing the size of your NVA to address persistent high CPU"
    description="Consider increasing the size of your NVA to address persistent high CPU"
    authors="evanba"
    ms.author="evanba"
    articleId="010692cc-0668-43fa-b7dc-6766efb22e59"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="CloudNet_NVA"
/>

# Consider increasing the size of your NVA to address persistent high CPU

---
{
  "recommendationOfferingId": "11be3d45-18f6-45bf-8df1-53a6164c24e5",
  "recommendationOfferingName": "NVA",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "010692cc-0668-43fa-b7dc-6766efb22e59",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://azphynet.kusto.windows.net').database('azphynetmds').NVAHighCPU",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Compute/virtualMachines",
  "recommendationFriendlyName": "NVAHighCPU",
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
  "learnMoreLink": "https://aka.ms/NVAHighCPU",
  "description": "Consider increasing the size of your NVA to address persistent high CPU",
  "longDescription": "When NVAs run at high CPU, packets can get dropped resulting in connection failures or high latency due to network retransmits. Your NVA is running at high CPU, so you should consider increasing the VM size as allowed by the NVA vendor's licensing requirements.",
  "potentialBenefits": "Reduce the odds of packet drops",
  "actions": [
    {
      "actionId": "24847536-5dab-4fb8-bbd4-cc8f8f27a717",
      "description": "Consider scaling up your NVA",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}",
        "menuid": "size"
      },
      "documentLink": ""
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "24847536-5dab-4fb8-bbd4-cc8f8f27a717",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      },
      "documentLink": ""
    }
  },
  "displayLabel": "NVA with high CPU",
  "additionalColumns": [{ "name": "HighestCPU", "title": "Maximum Hourly CPU" }],
  "tip": "",
  "costSavingInfo": "",
  "testData": "27b2ee0a-4093-4253-95b5-c595487ad66f,/subscriptions/27b2ee0a-4093-4253-95b5-c595487ad66f/resourceGroups/rgNVAHighCPU/providers/Microsoft.Compute/virtualMachines/test1, {\"HighestCPU\" : \"98.9\"}"
}
---
