<properties
    pageTitle="Use Ephemeral OS Disk VMs for more performance"
    description="For frequent Reimage operations, prefer IaaS VMs with Ephemeral OS Disk option"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="3531e7dd-6136-4f15-aa6f-0c935fcc1e2d_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
/>
# Create an Ephemeral OS Disk recommendation
---
{
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "3531e7dd-6136-4f15-aa6f-0c935fcc1e2d",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('Aznw').database('aznwcosmos').DeleteTestFunction",
    "dataSource": "Kusto",
    "refreshInterval": "01:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Low",
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
      "actionId": "05f3b618-5da8-431b-864c-1c08749c24bd",
      "description": "Transfer to using Ephemeral OS Disk",
      "actionType": "Document",
      "documentLink": "{externalLink}"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "002aa4f0-93b7-4535-b44c-372affc6470a",
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
