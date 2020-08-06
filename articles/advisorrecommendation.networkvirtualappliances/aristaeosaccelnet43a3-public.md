<properties
pageTitle="Arista Networks NVA Accelerated Networking alert"
description="Arista Networks NVA Accelerated Networking alert"
authors="vakr,scottnap"
ms.author="nvaeng"
articleId="43a3c88f-5bef-46c8-8e17-932159b3287d"
selfHelpType="advisorRecommendationMetadata"
cloudEnvironments="Public, usnat, ussec"
ownershipId="CloudNet_NVA"
/>
# Accelerated Networking Recommendation for Arista Networks vEOS Router
---
{
    "recommendationOfferingId": "92ec10d4-6c95-4aa3-b4c5-604d0e606985",
    "recommendationOfferingName": "NVA Engineering",
    "$schema": "AdvisorRecommendation",
    "recommendationTypeId": "43a3c88f-5bef-46c8-8e17-932159b3287d",
    "dataSourceMetadata": {
        "streamNamespace": "cluster('azphynet.kusto.windows.net').database('azphynetmds').GetVmListAristaAnReco",
        "dataSource": "Kusto",
        "refreshInterval": "0.12:00:00"
    },
    "recommendationCategory": "Performance",
    "recommendationImpact": "Medium",
    "recommendationResourceType": "Microsoft.Compute/virtualMachines",
    "recommendationFriendlyName": "AristaNVAAccelNet",
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
    "description": "Arista Networks vEOS Router may experience high CPU utilization, reduced throughput and high latency.",
    "longDescription": "We have identified that your Virtual Machine might be running a version of Arista Networks vEOS Router Image that is running older drivers for Accelerated Networking, which may cause the product to revert to using the standard, synthetic network interface which does not use Accelerated Networking. It is recommended that you upgrade to a newer version of the image that addresses this issue and enable Accelerated Networking. Please contact Arista Networks for further instructions on how to upgrade your Network Virtual Appliance Image.",
    "potentialBenefits": "You will not experience an unexpected degradation in network performance.",
    "actions": [
        {
            "actionId": "03b097a3-eede-4dd3-a69a-573f9eabb760",
            "description": "Contact Arista Networks support to upgrade vEOS Router image to 4.22.10 or later version.",
            "actionType": "Document",
            "documentLink": "https://www.arista.com/en/support/customer-support"
        }
    ],
    "displayLabel": "Accelerated Networking Recommendation for Arista Networks vEOS Router",
    "tip": "Upgrade Arista Networks vEOS Router image version to eliminate any unexpected degradation in network performance.",
    "testData":"0d5048c6-e9d8-4118-9a2d-fca00a351161,/subscriptions/0d5048c6-e9d8-4118-9a2d-fca00a351161/resourceGroups/linux-anosaxen-rg/providers/Microsoft.Compute/virtualMachines/1604linuxvm"
}
---