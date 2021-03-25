<properties
pageTitle="NVA Accellerated Networking enabled but not working"
description="NVA Accellerated Networking enabled but not working"
authors="scottnap,shafos,jeffcoo"
ms.author="nvaeng"
articleId="148fec38-cb1b-46ad-84b9-41233d07d4d9_public"
selfHelpType="advisorRecommendationMetadata"
cloudEnvironments="Public,USSEC,USNAT"
ownershipId="CloudNet_NVA"
/>
# Check for NVA Accellerated Networking enabled but not working
---
{
    "recommendationOfferingId": "92ec10d4-6c95-4aa3-b4c5-604d0e606985",
    "recommendationOfferingName": "NVA Engineering",
    "$schema": "AdvisorRecommendation",
    "recommendationTypeId": "148fec38-cb1b-46ad-84b9-41233d07d4d9",
    "dataSourceMetadata": {
        "streamNamespace": "cluster('azphynet.kusto.windows.net').database('azphynetmds').GetVmListANDisabled",
        "dataSource": "Kusto",
        "refreshInterval": "0.12:00:00"
    },
    "recommendationCategory": "OperationalExcellence",
    "recommendationImpact": "Medium",
    "recommendationResourceType": "Microsoft.Compute/virtualMachines",
    "recommendationFriendlyName": "GetVmListANDisabled",
    "recommendationMetadataState": "Active",
    "owner": {
        "email": "jeffcoog@microsoft.com",
        "icm": {
            "routingId": "MDM://Cloudnet/AzureNVA",
            "service": "Cloudnet",
            "team": "AzureNVA"
        },
        "serviceTreeId": "92ec10d4-6c95-4aa3-b4c5-604d0e606985"
    },
    "version": 1.0,
    "learnMoreLink": "https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli",
    "description": "NVA Accelerated Networking enabled but potentially not working.",
    "longDescription": "Desired state for Accelerated Networking is set to ‘true’ for one or more interfaces on this VM, but actual state for accelerated networking is not enabled.",
    "potentialBenefits": "Accelerated Networking offers improvements in network performance and reduced latency.",
    "actions": [
        {
            "actionId": "1110dba3-e2f3-485f-b29d-5e1f5386531f",
            "description": "Desired state for Accelerated Networking is set to ‘true’ for interfaces on this VM, but accelerated networking is not enabled. Please check with NVA Vendor that Accelerated Networking is supported for this SKU version.  If it is not supported, please check with the NVA Vendor for a version that does support Accelerated Networking.",
            "actionType": "Document",
            "documentLink": "https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli"
        }
    ],
    "displayLabel": "NVA Accellerated Networking enabled but not working",
    "tip": "Please review the information in the link",
    "testData": "0d5048c6-e9d8-4118-9a2d-fca00a351161,/subscriptions/0d5048c6-e9d8-4118-9a2d-fca00a351161/resourceGroups/TREXAUTH/providers/Microsoft.Compute/virtualMachines/TrexDeployer"
}
---
