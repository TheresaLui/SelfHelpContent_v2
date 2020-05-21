<properties
pageTitle="Palo Alto Networks NVA Accelerated Networking alert"
description="Palo Alto Networks NVA Accelerated Networking alert"
authors="vakr,scottnap"
ms.author="nvaeng"
articleId="e9a96e96-c68f-4604-b9ff-6b57ffb693da"
selfHelpType="advisorRecommendationMetadata"
cloudEnvironments="Public, usnat, ussec"
ownershipId="CloudNet_NVA"
/>
# Accelerated Networking Recommendation for Palo Alto Networks VM-Series Firewall
---
{
    "recommendationOfferingId": "92ec10d4-6c95-4aa3-b4c5-604d0e606985",
    "recommendationOfferingName": "NVA Engineering",
    "$schema": "AdvisorRecommendation",
    "recommendationTypeId": "e9a96e96-c68f-4604-b9ff-6b57ffb693da",
    "dataSourceMetadata": {
        "streamNamespace": "cluster('azphynet.kusto.windows.net').database('azphynetmds').GetVmlistPaloAltoAccelNete9a9",
        "dataSource": "Kusto",
        "refreshInterval": "0.12:00:00"
    },
    "recommendationCategory": "Performance",
    "recommendationImpact": "Medium",
    "recommendationResourceType": "Microsoft.Compute/virtualMachines",
    "recommendationFriendlyName": "PaloAltoNVAAccelNet",
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
    "description": "Palo Alto Networks VM-Series Firewall may experience high CPU utilization, reduced throughput and high latency.",
    "longDescription": "We have identified that your Virtual Machine might be running a version of Palo Alto Networks VM-Series Firewall Image that is running older drivers for Accelerated Networking, which may cause the product to revert to using the standard, synthetic network interface which does not use Accelerated Networking. It is recommended that you upgrade to a newer version of the image that addresses this issue and enable Accelerated Networking. Please contact Palo Alto Networks for further instructions on how to upgrade your Network Virtual Appliance Image.",
    "potentialBenefits": "You will not experience an unexpected degradation in network performance.",
    "actions": [
        {
            "actionId": "03b097a3-eede-4dd3-a69a-573f9eabb760",
            "description": "Contact Palo Alto Networks support to upgrade VM-Series Firewall image to 9.0.4 or later version.",
            "actionType": "Document",
            "documentLink": "https://www.paloaltonetworks.com/company/contact-support"
        }
    ],
    "displayLabel": "Accelerated Networking Recommendation for Palo Alto Networks VM-Series Firewall",
    "tip": "Upgrade Palo Alto Networks VM-Series Firewall image version to eliminate any unexpected degradation in network performance.",
    "testData":"0d5048c6-e9d8-4118-9a2d-fca00a351161,/subscriptions/0d5048c6-e9d8-4118-9a2d-fca00a351161/resourceGroups/vnet_peering_test/providers/Microsoft.Compute/virtualMachines/child-vm-2"
}
---