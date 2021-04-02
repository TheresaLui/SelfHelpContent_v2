<properties
pageTitle="NVA Max Flow Limit Alert"
description="NVA Max Flow Limit Alert"
authors="jeffcoo,scottnap"
ms.author="nvaeng"
articleId="f266acba-699d-4900-ae93-1bb488fd69df_public"
selfHelpType="advisorRecommendationMetadata"
cloudEnvironments="Public, usnat, ussec"
ownershipId="CloudNet_NVA"
/>
# Accelerated Networking Recommendation for NVA Max Flow Limit Hit
---
{
    "recommendationOfferingId": "92ec10d4-6c95-4aa3-b4c5-604d0e606985",
    "recommendationOfferingName": "NVA Engineering",
    "$schema": "AdvisorRecommendation",
    "recommendationTypeId": "f266acba-699d-4900-ae93-1bb488fd69df",
    "dataSourceMetadata": {
        "streamNamespace": "cluster('azphynet.kusto.windows.net').database('azphynetmds').NVAMaxFlowLimit",
        "dataSource": "Kusto",
        "refreshInterval": "0.12:00:00"
    },
    "recommendationCategory": "Performance",
    "recommendationImpact": "Medium",
    "recommendationResourceType": "Microsoft.Compute/virtualMachines",
    "recommendationFriendlyName": "NvaMaxFlowLimit",
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
    "version": 1.1,
    "learnMoreLink": "https://docs.microsoft.com/azure/virtual-network/virtual-machine-network-throughput",
    "description": "NVA may see traffic loss due to hitting the maximum number of flows.",
    "longDescription": "Packet loss has been observed for this Virtual Machine due to hitting or exceeding the maximum number of flows for a VM instance of this size on Azure",
    "potentialBenefits": "You will see increased performance",
    "actions": [
        {
            "actionId": "0ba9ab1e-ab7e-41c7-a346-fee71fa2d34c",
            "description": "NVA VM Instance Maximum Flow Limit",
            "actionType": "Document",
            "documentLink": "https://docs.microsoft.com/azure/virtual-network/virtual-machine-network-throughput"
        }
    ],
    "displayLabel": "NVA VM Instance Maximum Flow Limit",
    "tip": "Scale to use more VMs or increase the VM size to more than 8 cores",
    "testData":"0d5048c6-e9d8-4118-9a2d-fca00a351161,/subscriptions/0d5048c6-e9d8-4118-9a2d-fca00a351161/resourceGroups/TREXAUTH/providers/Microsoft.Compute/virtualMachines/TrexDeployer"
}
---