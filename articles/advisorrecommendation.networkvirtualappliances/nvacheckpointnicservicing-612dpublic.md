<properties
pageTitle="Checkpoint NVA Image known issue alert"
description="Checkpoint NVA Image known issue alert"
authors="scottnap,shafos,jeffcoo"
ms.author="nvaeng"
articleId="4ffc56f4-3fa7-49e2-adaa-e0c1960e612d_public"
selfHelpType="advisorRecommendationMetadata"
cloudEnvironments="Public, usnat, ussec"
ownershipId="CloudNet_NVA"
/>
# Known issue with CheckPoint Network Virtual Appliance image version
---
{
    "recommendationOfferingId": "92ec10d4-6c95-4aa3-b4c5-604d0e606985",
    "recommendationOfferingName": "NVA Engineering",
    "$schema": "AdvisorRecommendation",
    "recommendationTypeId": "4ffc56f4-3fa7-49e2-adaa-e0c1960e612d",
    "dataSourceMetadata": {
        "streamNamespace": "cluster('azphynet.kusto.windows.net').database('azphynetmds').NvaCheckpointNicServicing",
        "dataSource": "Kusto",
        "refreshInterval": "0.12:00:00"
    },
    "recommendationCategory": "OperationalExcellence",
    "recommendationImpact": "High",
    "recommendationResourceType": "Microsoft.Compute/virtualMachines",
    "recommendationFriendlyName": "NvaCheckpointNicServicing",
    "recommendationMetadataState": "Active",
    "owner": {
        "email": "nvaeng@microsoft.com",
        "icm": {
            "routingId": "MDM://Cloudnet/AzureNVA",
            "service": "Cloudnet",
            "team": "AzureNVA"
        },
        "serviceTreeId": "92ec10d4-6c95-4aa3-b4c5-604d0e606985"
    },
    "version": 1.10,
    "learnMoreLink": "https://supportcenter.checkpoint.com/supportcenter/portal",
    "description": "An Azure environment update has been rolled out that may affect you Checkpoint FW.",
    "longDescription": "The image version of the Checkpoint firewall installed may have been affected by the recent Azure environment update. A kernel panic resulting in a reboot to factory defaults can occur in certain circumstances.",
    "potentialBenefits": "Ensure business continuity through better network connectivity.",
    "actions": [
        {
            "actionId": "ddf4ef49-f502-4d47-b865-ac780a769229",
            "description": "Contact Checkpoint support to upgrade Network Virtual Appliance image version",
            "actionType": "Document",
            "documentLink": "https://supportcenter.checkpoint.com/supportcenter/portal"
        }
    ],
    "displayLabel": "Known issue for Checkpoint Network Virtual Appliance image version with NIC servicing",
    "tip": "Upgrade Network Virtual Appliance image to ensure business continuity.",
    "additionalColumns": [
        {
          "name": "Duration",
          "title": "Event Duration"
        },
        {
          "name": "startTime",
          "title": "Event Start Time"
        }
    ],
    "testData": "0d5048c6-e9d8-4118-9a2d-fca00a351161,/subscriptions/0d5048c6-e9d8-4118-9a2d-fca00a351161/resourceGroups/TREXAUTH/providers/Microsoft.Compute/virtualMachines/TrexDeployer"
}
---
