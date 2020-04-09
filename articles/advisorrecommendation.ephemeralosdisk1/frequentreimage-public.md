<properties
    pageTitle="Use Ephemeral OS Disk VMs for Cost Savings"
    description="For Short-Lived VMs or VMs with Stateless workload, prefer IaaS VMs with Ephemeral OS Disk option"
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
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Compute/virtualMachines",
  "recommendationFriendlyName": "EphemeralOsDisk",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "ramsaic@microsoft.com",
    "icm": {
      "routingId": "MDM://OneFleet Node/AzureHost-Agent-Sev-3-4",
      "service": "OneFleet Node",
      "team": "AzureHost-Agent-Sev-3-4"
    },
    "serviceTreeId": "12345678-9012-3456-7890-123456789012"
  },
  "ingestionClientIdentities": ["3cf3c489-3096-425a-940e-abd5f0c52c73"],
  "version": 3.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/virtual-machines/windows/ephemeral-os-disks",
  "description": "(Use Ephemeral OS Disk VMs for more performance",
  "longDescription": "For short-lived VMs or VMs with stateless workloads, prefer IaaS VMs with Ephemeral OS Disk option",
  "potentialBenefits": "This will reduce the Cost, with zero charge on OS disk. It will also improve the waiting time involved with multiple Creates/Deletes. Instead can adopt the much quicker Reimage VM approach, to wipe the contents on OS disk and reset it to fresh clean state, just like a brand new VM",
  "actions": [
    {
      "actionId": "5093444f-7ef5-41ea-9fac-d9c94fcdb911",
      "description": "Transfer to using Ephemeral OS Disk",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/virtual-machines/windows/ephemeral-os-disks"
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
  "testData": "9ff53016-3d9d-4e40-94b0-873871ac1b07,/subscriptions/9ff53016-3d9d-4e40-94b0-873871ac1b07/resourceGroups/TestAADRecco-RG-1/providers/Microsoft.Compute/virtualMachines/TestWinEphmVM"	,
  "tip": "This will reduce the Cost, with zero charge on OS disk. Also improves the waiting time involved with multiple Creates/Deletes. Instead can adopt the much quicker Reimage VM approach, to wipe the contents on OS disk and reset it to fresh clean state, just like a brand new VM)"
}
---
