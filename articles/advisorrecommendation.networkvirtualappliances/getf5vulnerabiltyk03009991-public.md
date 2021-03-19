<properties
pageTitle="NVA Image no longer suppported and not available in Market Place"
description="NVA Image no longer suppported and not available in Market Place"
authors="scottnap,shafos,jeffcoo"
ms.author="nvaeng"
articleId="a71bfb94-b9e8-473e-b0a5-9fafc92cdb05_public"
selfHelpType="advisorRecommendationMetadata"
cloudEnvironments="Public,USSEC,USNAT"
ownershipId="CloudNet_NVA"
/>
# Known issue with CheckPoint Network Virtual Appliance image version
---
{
    "recommendationOfferingId": "92ec10d4-6c95-4aa3-b4c5-604d0e606985",
    "recommendationOfferingName": "NVA Engineering",
    "$schema": "AdvisorRecommendation",
    "recommendationTypeId": "a71bfb94-b9e8-473e-b0a5-9fafc92cdb05",
    "dataSourceMetadata": {
        "streamNamespace": "cluster('azphynet.kusto.windows.net').database('azphynetmds').GetF5BigipListK03009991",
        "dataSource": "Kusto",
        "refreshInterval": "0.12:00:00"
    },
    "recommendationCategory": "OperationalExcellence",
    "recommendationImpact": "Medium",
    "recommendationResourceType": "Microsoft.Compute/virtualMachines",
    "recommendationFriendlyName": "GetF5EolImages",
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
    "learnMoreLink": "https://support.f5.com/csp/article/K03009991",
    "description": "The iControl REST interface has an unauthenticated remote command execution vulnerability.",
    "longDescription": "This vulnerability allows for unauthenticated attackers with network access to the iControl REST interface, through the BIG-IP management interface and self IP addresses, to execute arbitrary system commands, create or delete files, and disable services. This vulnerability can only be exploited through the control plane and cannot be exploited through the data plane. Exploitation can lead to complete system compromise. The BIG-IP system in Appliance mode is also vulnerable",
    "potentialBenefits": "Avoid security incidents and unauthorized access to VM.",
    "actions": [
        {
            "actionId": "e33cd53b-b352-41fd-a89e-45f71d5b9680",
            "description": "Please contact F5 to upgrade to the latest recommended image version",
            "actionType": "Document",
            "documentLink": "https://www.f5.com/services/support"
        }
    ],
    "displayLabel": "NVA Image no longer suppported and not available in Market Place",
    "tip": "Please review the information in the link ",
 
    "testData": "0d5048c6-e9d8-4118-9a2d-fca00a351161,/subscriptions/0d5048c6-e9d8-4118-9a2d-fca00a351161/resourceGroups/TREXAUTH/providers/Microsoft.Compute/virtualMachines/TrexDeployer
}
---
