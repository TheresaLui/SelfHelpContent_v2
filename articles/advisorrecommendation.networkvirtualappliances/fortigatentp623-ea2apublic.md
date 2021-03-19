<properties
pageTitle="FortiGate NVA Image known issue alert"
description="FortiGate NVA Image known issue alert"
authors="scottnap,shafos,jeffcoo"
ms.author="nvaeng"
articleId="75930197-b082-4f29-aff1-96d58cf5ea2a_public"
selfHelpType="advisorRecommendationMetadata"
cloudEnvironments="Public, usnat, ussec"
ownershipId="CloudNet_NVA"
/>
# Known issue with Check Point Network Virtual Appliance image version
---
{
    "recommendationOfferingId": "92ec10d4-6c95-4aa3-b4c5-604d0e606985",
    "recommendationOfferingName": "NVA Engineering",
    "$schema": "AdvisorRecommendation",
    "recommendationTypeId": "75930197-b082-4f29-aff1-96d58cf5ea2a",
    "dataSourceMetadata": {
        "streamNamespace": "cluster('azphynet.kusto.windows.net').database('azphynetmds').GetVmlistFortigateNtpIssue",
        "dataSource": "Kusto",
        "refreshInterval": "0.12:00:00"
    },
    "recommendationCategory": "OperationalExcellence",
    "recommendationImpact": "High",
    "recommendationResourceType": "Microsoft.Compute/virtualMachines",
    "recommendationFriendlyName": "GetVmlistFortigateNtpIssue",
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
    "learnMoreLink": "https://docs.fortinet.com/document/fortigate/6.2.3/fortios-release-notes/236526/known-issues",
    "description": "Excessive NTP client traffic caused by frequent DNS lookups and NTP sync for new servers, which happens often on some global NTP servers.",
    "longDescription": "Excessive NTP client traffic caused by frequent DNS lookups and NTP sync for new servers, which happens often on some global NTP servers. This can be viewed as malicious traffic and blocked by the DDOS service in the Azure environment",
    "potentialBenefits": "Ensure business continuity through better network connectivity.",
    "actions": [
        {
            "actionId": "86a17c8a-c912-4139-b0b8-184b81722f0b",
            "description": "Contact Fortinet support to upgrade Network Virtual Appliance image version",
            "actionType": "Document",
            "documentLink": "https://www.fortinet.com/support"
        }
    ],
    "displayLabel": "Known NTP Issue with Fortigate Network Virtual Appliance image version",
    "tip": "Upgrade Network Virtual Appliance image to ensure business continuity.",
    "testData": "0d5048c6-e9d8-4118-9a2d-fca00a351161,/subscriptions/0d5048c6-e9d8-4118-9a2d-fca00a351161/resourceGroups/TREXAUTH/providers/Microsoft.Compute/virtualMachines/TrexDeployer"
}
---
