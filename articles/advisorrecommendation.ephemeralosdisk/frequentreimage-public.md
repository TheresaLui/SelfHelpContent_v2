<properties
    pageTitle="Use Ephemeral OS Disk VMs for more performance"
    description="For frequent Reimage operations, prefer IaaS VMs with Ephemeral OS Disk option"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="6bd863c0-af9a-4426-bf9d-26a0ee94d4d7_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
/>
# Create an Ephemeral OS Disk recommendation
---
{
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "6bd863c0-af9a-4426-bf9d-26a0ee94d4d7",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://azcrp.kusto.windows.net').database('crp_allprod').DeleteTestFunction",
    "dataSource": "Kusto",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Compute/virtualMachines",
  "recommendationFriendlyName": "EphemeralOsDisk",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "ramsaic@microsoft.com",
    "icm": {
      "routingId": "MDM://Azure/Billing",
      "service": "Azure",
      "team": "Azure"
    },
    "serviceTreeId": "12345678-9012-3456-7890-123456789012"
  },
  "ingestionClientIdentities": [],
  "version": 1.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/virtual-machines/windows/ephemeral-os-disks",
  "description": "Use Ephemeral OS Disk VMs for more performance",
  "longDescription": "For frequent Reimage operations, prefer IaaS VMs with Ephemeral OS Disk option",
  "potentialBenefits": "This will improve VM Reimage duration to a great extend(around one half of duration taken by IaaS VM)",
  "actions": [
    {
      "actionId": "20444076-b272-4435-ab58-c6f961255e11",
      "description": "Transfer to using Ephemeral OS Disk",
      "actionType": "Document",
      "documentLink": "{externalLink}"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "492cb098-5ab6-4f69-aaf8-67478a2f5429",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Use Ephemeral OS Disk",
  "additionalColumns": [],
  "testData": "9ff53016-3d9d-4e40-94b0-873871ac1b07,/subscriptions/9ff53016-3d9d-4e40-94b0-873871ac1b07/resourceGroups/TestEphmVmssRG-1/providers/Microsoft.Compute/virtualMachines/vmssteste_0"	,
  "tip": "This will improve VM Reimage duration to a great extend(around one half of duration taken by IaaS VM)"
}
---
