<properties
    pageTitle="Use Ephemeral OS Disk VMs for more performance"
    description="For frequent Reimage operations, prefer IaaS VMs with Ephemeral OS Disk option"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="dc045941-8e65-437b-992b-1f0acd28bb6e_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
/>
# Create an Ephemeral OS Disk recommendation
---
{
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "dc045941-8e65-437b-992b-1f0acd28bb6e",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "dataSource": "SAS"
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
  "ingestionClientIdentities": [“00000000-0000-0000-0000-000000000001", ”00000000-0000-0000-0000-000000000002"],
  "version": 1.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/virtual-machines/windows/ephemeral-os-disks",
  "description": "(V2)Use Ephemeral OS Disk VMs for more performance",
  "longDescription": "(V2)For frequent Reimage operations, prefer IaaS VMs with Ephemeral OS Disk option",
  "potentialBenefits": "This will improve VM Reimage duration to a great extent(around one half of duration taken by IaaS VM)",
  "actions": [
    {
      "actionId": "5093444f-7ef5-41ea-9fac-d9c94fcdb911",
      "description": "Transfer to using Ephemeral OS Disk",
      "actionType": "Document",
      "documentLink": "{externalLink}"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "a14e9bb9-bff2-4457-bc88-cd84218e51be",
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
  "testData": "9ff53016-3d9d-4e40-94b0-873871ac1b07,/subscriptions/9ff53016-3d9d-4e40-94b0-873871ac1b07"	,
  "tip": "This will improve VM Reimage duration to a great extent(around one half of duration taken by IaaS VM)"
}
---
