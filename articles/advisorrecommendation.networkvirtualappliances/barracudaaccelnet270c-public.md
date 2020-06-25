<properties
pageTitle="Barracuda Networks NVA Accelerated Networking alert"
description="Barracuda Networks NVA Accelerated Networking alert"
authors="vakr,scottnap"
ms.author="nvaeng"
articleId="270c5ab3-31d0-461f-bf8d-55d739552d31"
selfHelpType="advisorRecommendationMetadata"
cloudEnvironments="Public, usnat, ussec"
ownershipId="CloudNet_NVA"
/>
# Accelerated Networking Recommendation for Barracuda Networks NextGen Firewall
---
{
    "recommendationOfferingId": "92ec10d4-6c95-4aa3-b4c5-604d0e606985",
    "recommendationOfferingName": "NVA Engineering",
    "$schema": "AdvisorRecommendation",
    "recommendationTypeId": "270c5ab3-31d0-461f-bf8d-55d739552d31",
    "dataSourceMetadata": {
        "streamNamespace": "cluster('azphynet.kusto.windows.net').database('azphynetmds').GetVmlistBarracudaAccelNet270c",
        "dataSource": "Kusto",
        "refreshInterval": "0.12:00:00"
    },
    "recommendationCategory": "Performance",
    "recommendationImpact": "Medium",
    "recommendationResourceType": "Microsoft.Compute/virtualMachines",
    "recommendationFriendlyName": "BarracudaNVAAccelNet",
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
    "description": "Barracuda Networks NextGen Firewall may experience high CPU utilization, reduced throughput and high latency.",
    "longDescription": "We have identified that your Virtual Machine might be running a version of Barracuda Networks NextGen Firewall Image that is running older drivers for Accelerated Networking, which may cause the product to revert to using the standard, synthetic network interface which does not use Accelerated Networking. It is recommended that you upgrade to a newer version of the image that addresses this issue and enable Accelerated Networking. Please contact Barracuda Networks for further instructions on how to upgrade your Network Virtual Appliance Image.",
    "potentialBenefits": "You will not experience an unexpected degradation in network performance.",
    "actions": [
        {
            "actionId": "03b097a3-eede-4dd3-a69a-573f9eabb760",
            "description": "Contact Barracuda Networks support to upgrade NextGen Firewall image to 8.0.0047504 version or later which support newer drivers.",
            "actionType": "Document",
            "documentLink": "https://www.barracuda.com/support"
        }
    ],
    "displayLabel": "Accelerated Networking Recommendation for Barracuda Networks NextGen Firewall",
    "tip": "Upgrade Barracuda Networks NextGen Firewall image version to eliminate any unexpected degradation in network performance.",
    "testData":"0d5048c6-e9d8-4118-9a2d-fca00a351161,/subscriptions/0d5048c6-e9d8-4118-9a2d-fca00a351161/resourceGroups/np-g-7e297f3b-7394-438e-b79c-e92e49cd62be/providers/Microsoft.Compute/virtualMachines/c-ubuntu-management"
}
---