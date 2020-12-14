<properties
    pageTitle="Use Ephemeral OS Disk for cost savings" 
    description="Ephemeral OS disks are created on the local virtual machine storage instead of the remote Azure Storage. Ephemeral OS disk is free and you incur no storage cost for OS disk. With Ephemeral OS disk, you get lower read/write latency to the OS disk and faster VM reimage time. It also provides faster VM reimage operation to wipe the contents on OS disk and reset the VM to its original state. This significantly reduces the idle time involved with multiple VM create/delete operations. Ephemeral OS disks are recommended for VMs where the OS disk is stateless i.e. applications which are tolerant of individual VM failures." 
    authors="EphemeralOSDiskvTeam" 
    ms.author="EphemeralOSDiskvTeam" 
    articleId="dc045941-8e65-437b-992b-1f0acd28bb6e_USNat" 
    selfHelpType="advisorRecommendationMetadata" 
    cloudEnvironments="USNat" 
    ownershipId="Compute_VirtualMachines"
/>

# Create an Ephemeral OS Disk recommendation for USNat Cloud
---
{
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "dc045941-8e65-437b-992b-1f0acd28bb6e",
  "dataSourceMetadata": {
    "schemaVersion": 2,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Subscriptions/subscriptions",
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
    "serviceTreeId": "5d0f2841-795b-49c6-9ab1-c2195fc9a4ea"
  },
  "ingestionClientIdentities": [
    "937c4bb1-6cb1-4613-8d94-3fe6874c9819"
  ],
  "version": 4,
  "learnMoreLink": "https://docs.microsoft.com/azure/virtual-machines/windows/ephemeral-os-disks",
  "description": "Use Virtual Machines with Ephemeral OS Disk enabled to save cost and get better performance",
  "longDescription": "With Ephemeral OS Disk, Customers get these benefits: Save on storage cost for OS disk. Get lower read/write latency to OS disk. Faster VM Reimage operation by resetting OS (and Temporary disk) to its original state. It is more preferrable to use Ephemeral OS Disk for short-lived IaaS VMs or VMs with stateless workloads",
  "potentialBenefits": "Reduced storage cost, lower read/write latency, faster reimage operation for OS disk. More preferrable for short-lived IaaS VMs or VMs with stateless workloads",
  "actions": [
    {
      "actionId": "0188fd39-3cce-4990-9188-8c52b4af2d34",
      "description": "Use Virtual Machines with Ephemeral OS Disk enabled",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/virtual-machines/windows/ephemeral-os-disks"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "d5ec5201-8058-448c-948a-463db9c2f980",
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
  "testData": "9ff53016-3d9d-4e40-94b0-873871ac1b07,/subscriptions/9ff53016-3d9d-4e40-94b0-873871ac1b07",
  "tip": "Ephemeral OS disk incurs no storage cost for OS disk and provides lower read/write latency to the OS disk. It also provides faster VM reimage operation to wipe the contents on OS disk and reset the VM to its original state. This significantly reduces the idle time involved with multiple VM create/delete operations."
}
---
