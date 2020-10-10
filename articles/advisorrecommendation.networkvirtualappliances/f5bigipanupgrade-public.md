<properties
pageTitle="NVA Accelerated Networking upgrade alert recommendation"
description="NVA Accelerated Networking upgrade recommendation"
authors="jeffcoo,scottnap"
ms.author="nvaeng"
articleId="48432aa1-f081-4de9-9e7e-e2e6a7d354bb_Public"
selfHelpType="advisorRecommendationMetadata"
cloudEnvironments="Public, usnat, ussec"
ownershipId="CloudNet_NVA"
/>
# Accelerated Networking Recommendation for F5 BigIp
---
{
    "recommendationOfferingId": "92ec10d4-6c95-4aa3-b4c5-604d0e606985",
    "recommendationOfferingName": "NVA Engineering",
    "$schema": "AdvisorRecommendation",
    "recommendationTypeId": "48432aa1-f081-4de9-9e7e-e2e6a7d354bb",
    "dataSourceMetadata": {
        "streamNamespace": "cluster('azphynet.kusto.windows.net').database('azphynetmds').GetF5BigIpVmListANUpgradeReco",
        "dataSource": "Kusto",
        "refreshInterval": "0.12:00:00"
    },
    "recommendationCategory": "Performance",
    "recommendationImpact": "Medium",
    "recommendationResourceType": "Microsoft.Compute/virtualMachines",
    "recommendationFriendlyName": "F5BigIpANUpgradeRecommendation",
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
    "version": 1.0,
    "learnMoreLink": "https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli#enable-accelerated-networking-on-existing-vms",
    "description":"Update to the latest version of your F5 BigIp product for Accelerated Networking support." ,
    "longDescription": "We have identified that your Virtual Machine might be running a version of software image that is running older drivers for Accelerated Networking (AN). It has a synthetic network interface which, either, is not AN capable or is not compatible with all Azure hardware. It is recommended that you upgrade to the latest version of the image that addresses this issue and enable Accelerated Networking. Please contact your vendor for further instructions on how to upgrade your Network Virtual Appliance Image.",
    "potentialBenefits": "Faster network throughput with lower latency.",
    "actions": [
        {
            "actionId": "e426a334-7c3c-4770-9fa2-b7419a97a9d1",
            "description": "Contact Vendor support to upgrade NVA image to latest recommended version",
            "actionType": "Document",
            "documentLink": "https://www.f5.com/services/support"
        }
    ],
    "displayLabel": "Upgrade your Network Virtual Appliance Version to enable Accelerated Networking on all platforms.",
    "tip": "Upgrade your Network Virtual Appliance image version to eliminate any unexpected degradation in network performance.",
    "testData":"0d5048c6-e9d8-4118-9a2d-fca00a351161,/subscriptions/0d5048c6-e9d8-4118-9a2d-fca00a351161/resourceGroups/np-g-7e297f3b-7394-438e-b79c-e92e49cd62be/providers/Microsoft.Compute/virtualMachines/ciscoasafwasavha-a"
}
---