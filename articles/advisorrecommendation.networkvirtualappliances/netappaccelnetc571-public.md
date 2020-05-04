<properties
pageTitle="NetApp NVA Accelerated Networking alert"
description="NetApp NVA Accelerated Networking alert"
authors="vakr,scottnap"
ms.author="nvaeng"
articleId="c571b9b2-fe79-4785-8083-30b7b57a4f3d"
selfHelpType="advisorRecommendationMetadata"
cloudEnvironments="Public"
ownershipId="CloudNet_NVA"
/>
# Accelerated Networking Recommendation for NetApp Cloud Volumes ONTAP
---
{
    "recommendationOfferingId": "92ec10d4-6c95-4aa3-b4c5-604d0e606985",
    "recommendationOfferingName": "NVA Engineering",
    "$schema": "AdvisorRecommendation",
    "recommendationTypeId": "c571b9b2-fe79-4785-8083-30b7b57a4f3d",
    "dataSourceMetadata": {
        "streamNamespace": "cluster('azphynet.kusto.windows.net').database('azphynetmds').GetVmlistNetAppAccelNetc571",
        "dataSource": "Kusto",
        "refreshInterval": "0.12:00:00"
    },
    "recommendationCategory": "Performance",
    "recommendationImpact": "Medium",
    "recommendationResourceType": "Microsoft.Compute/virtualMachines",
    "recommendationFriendlyName": "NetAppNVAAccelNet",
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
    "description": "NetApp Cloud Volumes ONTAP may experience reduced network throughput and high latency",
    "longDescription": "We have identified that your Virtual Machine might be running a version of NetApp Cloud Volumes ONTAP Image that is known to experience low network throughput and high latency. It is recommended that you upgrade to a newer version of the image that addresses this issue and enable Accelerated Networking. Please contact NetApp for further instructions on how to upgrade your Network Virtual Appliance Image.",
    "potentialBenefits": "Improves network throughput while reducing latency and jitter",
    "actions": [
        {
            "actionId": "03b097a3-eede-4dd3-a69a-573f9eabb760",
            "description": "Contact NetApp support to upgrade Cloud Volumes ONTAP image version",
            "actionType": "Document",
            "documentLink": "https://mysupport.netapp.com/site/"
        }
    ],
    "displayLabel": "Accelerated Networking Recommendation for NetApp Cloud Volumes ONTAP",
    "tip": "Upgrade NetApp Cloud Volumes ONTAP image version to improve network throughput while reducing latency and jitter.",
    "testData":"0d5048c6-e9d8-4118-9a2d-fca00a351161,/subscriptions/0d5048c6-e9d8-4118-9a2d-fca00a351161/resourceGroups/vnet_peering_test/providers/Microsoft.Compute/virtualMachines/child-vm-1"
}
---