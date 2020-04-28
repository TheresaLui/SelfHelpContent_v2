<properties
pageTitle="Check Point NVA Image known issue alert"
description="Check Point NVA Image known issue alert"
authors="vakr,scottnap,shafos"
ms.author="nvaeng"
articleId="bfd7005c-26f0-4418-86cf-b5dc9665d68b"
selfHelpType="advisorRecommendationMetadata"
cloudEnvironments="Public"
/>
# Known issue with Check Point Network Virtual Appliance image version
---
{
    "recommendationOfferingId": "92ec10d4-6c95-4aa3-b4c5-604d0e606985",
    "recommendationOfferingName": "NVA Engineering",
    "$schema": "AdvisorRecommendation",
    "recommendationTypeId": "bfd7005c-26f0-4418-86cf-b5dc9665d68b",
    "dataSourceMetadata": {
        "streamNamespace": "cluster('azphynet.kusto.windows.net').database('azphynetmds').GetVmlistCheckPointbfd7",
        "dataSource": "Kusto",
        "refreshInterval": "0.12:00:00"
    },
    "recommendationCategory": "HighAvailability",
    "recommendationImpact": "High",
    "recommendationResourceType": "Microsoft.Compute/virtualMachines",
    "recommendationFriendlyName": "NVAKnownIssues",
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
    "learnMoreLink": "https://supportcenter.checkpoint.com/supportcenter/portal?eventSubmit_doGoviewsolutiondetails=&solutionid=sk151752&partition=Advanced&product=CloudGuard",
    "description": "Check Point Virtual Machine may lose Network Connectivity.",
    "longDescription": "We have identified that your Virtual Machine might be running a version of Check Point image that has been known to lose network connectivity in the event of a platform servicing operation. It is recommended that you upgrade to a newer version of the image that addresses this issue. Please contact Check Point for further instructions on how to upgrade your image.",
    "potentialBenefits": "Ensure business continuity through better network connectivity.",
    "actions": [
        {
            "actionId": "1a62b6c5-39e7-4a19-a07b-d0eaa38d47b6",
            "description": "Contact Check Point support to upgrade Check Point Network Virtual Appliance image",
            "actionType": "Document",
            "documentLink": "https://www.checkpoint.com/support-services/contact-support/"
        }
    ],
    "displayLabel": "Known Issue with Check Point Network Virtual Appliance image version",
    "tip": "Upgrade Network Virtual Appliance image to ensure buisiness continuity.",
    "testData": "0d5048c6-e9d8-4118-9a2d-fca00a351161,/subscriptions/0d5048c6-e9d8-4118-9a2d-fca00a351161/resourceGroups/bigipha_rg/providers/Microsoft.Compute/virtualMachines/bigiphatest-f5vm010"
}
---
