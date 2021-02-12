<properties
pageTitle="Cisco NVA Accelerated Networking alert"
description="Cisco NVA Accelerated Networking alert"
authors="vakr,scottnap"
ms.author="nvaeng"
articleId="7747ce74-9209-4fe4-8dd8-6cd74ac1c9ba_public"
selfHelpType="advisorRecommendationMetadata"
cloudEnvironments="Public, usnat, ussec"
ownershipId="CloudNet_NVA"
/>
# Accelerated Networking Recommendation for Cisco Cloud Services Router 1000V
---
{
    "recommendationOfferingId": "92ec10d4-6c95-4aa3-b4c5-604d0e606985",
    "recommendationOfferingName": "NVA Engineering",
    "$schema": "AdvisorRecommendation",
    "recommendationTypeId": "7747ce74-9209-4fe4-8dd8-6cd74ac1c9ba",
    "dataSourceMetadata": {
        "streamNamespace": "cluster('azphynet.kusto.windows.net').database('azphynetmds').GetVmListCiscoAnReco",
        "dataSource": "Kusto",
        "refreshInterval": "0.12:00:00"
    },
    "recommendationCategory": "Performance",
    "recommendationImpact": "Medium",
    "recommendationResourceType": "Microsoft.Compute/virtualMachines",
    "recommendationFriendlyName": "CiscoCSRNVAAccelNet",
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
    "description": "Cisco Cloud Services Router 1000V may experience high CPU utilization, reduced throughput and high latency.",
    "longDescription": "We have identified that your Virtual Machine might be running a version of Cisco Cloud Services Router 1000V Image that is running older drivers for Accelerated Networking, which may cause the product to revert to using the standard, synthetic network interface which does not use Accelerated Networking. It is recommended that you upgrade to a newer version of the image that addresses this issue and enable Accelerated Networking. Please contact Cisco for further instructions on how to upgrade your Network Virtual Appliance Image.",
    "potentialBenefits": "You will not experience an unexpected degradation in network performance.",
    "actions": [
        {
            "actionId": "03b097a3-eede-4dd3-a69a-573f9eabb760",
            "description": "Contact Cisco support to upgrade Cloud Services Router 1000V image to 16.12.0 or later version.",
            "actionType": "Document",
            "documentLink": "https://www.cisco.com/c/en/us/support/index.html"
        }
    ],
    "displayLabel": "Accelerated Networking Recommendation for Cisco Cloud Services Router 1000V",
    "tip": "Upgrade Cisco Cloud Services Router 1000V image version to eliminate any unexpected degradation in network performance.",
    "testData":"0d5048c6-e9d8-4118-9a2d-fca00a351161,/subscriptions/0d5048c6-e9d8-4118-9a2d-fca00a351161/resourceGroups/np-g-7e297f3b-7394-438e-b79c-e92e49cd62be/providers/Microsoft.Compute/virtualMachines/ciscoasafwasavha-a"
}
---
