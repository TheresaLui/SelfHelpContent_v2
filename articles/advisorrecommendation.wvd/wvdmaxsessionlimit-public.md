<properties
    pageTitle="Change the max session limit for your depth first load balanced host pool to improve VM performance"
    description="Change the max session limit for your depth first load balanced host pool to improve VM performance"
    authors="sefriend"
    ms.author="rdinfra"
    articleId="2cc17306-822e-45b1-8d7f-5b0d2f2cccdb_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, ussec, usnat"
    ownershipId="Windows_Virtual_Desktop"
/>
# Change the Max Session Limit
---
{
    "recommendationOfferingId": "1132b618-fefe-40a0-9256-e685ff575ac7",
    "recommendationOfferingName": "Windows Virtual Desktop",
    "$schema": "AdvisorRecommendation",
    "recommendationTypeId": "2cc17306-822e-45b1-8d7f-5b0d2f2cccdb",
    "dataSourceMetadata": {
        "streamNamespace": "cluster('https://rdsprodus2.westus2.kusto.windows.net').database('WVD').HostPoolDepthFirstNeedsBetterLimits",
        "dataSource": "Kusto",
        "refreshInterval": "0.12:00:00"
    },
    "recommendationCategory": "Performance",
    "recommendationImpact": "High",
    "recommendationResourceType": "Microsoft.DesktopVirtualization/hostpools",
    "recommendationFriendlyName": "ChangeMaxSessionLimitForDepthFirstHostPool",
    "recommendationMetadataState": "Active",
    "owner": {
        "email": "rdinfra@microsoft.com",
        "icm": {
            "routingId": "mdm://adspartner/VirtualDesktop",
            "service": "Windows Virtual Desktop",
            "team": "Windows Virtual Desktop"
        },
        "serviceTreeId": "362c0db7-c08b-4471-93ef-c90effc930dd"
    },
    "ingestionClientIdentities": [],
    "version": 1.0,
    "learnMoreLink": "https://docs.microsoft.com/azure/virtual-desktop/configure-host-pool-load-balancing",
    "description": "Change the max session limit for your depth first load balanced host pool to improve VM performance ",
    "longDescription": "Depth first load balancing uses the max session limit to determine the maximum number of users that can have concurrent sessions on a single session host. If the max session limit is too high, all user sessions will be directed to the same session host and this may cause performance and reliability issues. Therefore, when setting a host pool to have depth first load balancing, you should also set an appropriate max session limit according to the configuration of your deployment and capacity of your VMs. To fix this, open your host pool's properties and change the value next to the \"Max session limit\" setting.",
    "potentialBenefits": "Ensure session host functional stability, reliability, and performance when using Windows Virtual Desktop service",
    "actions": [
        {
            "actionId": "da1af884-c4e0-4b08-a159-9a2654b9468c",
            "description": "Change host pool max session limit",
            "actionType": "Blade",
            "extensionName": "Microsoft_Azure_WVD",
            "bladeName": "HostpoolOverviewBlade",
            "metadata": {
                "id": "{resourceId}"
            }
        }
    ],
    "resourceMetadata": {
        "action": {
            "actionId": "aed8be6b-de48-4d24-a1ba-6efe42489fbd",
            "actionType": "Blade",
            "extensionName": "Microsoft_Azure_WVD",
            "bladeName": "HostpoolOverviewBlade",
            "metadata": {
                "id": "{resourceId}"
            }
        }
    },
    "displayLabel": "Change max session limit for depth first load balanced host pool",
    "additionalColumns": [
        {
            "name": "hostPool",
            "title": "Host Pool"
        },
        {
            "name": "maxSessions",
            "title": "# default sessions used"
        }
    ],
    "tip": "Change the max session limit for your depth first load balanced host pool to improve VM performance."
}
---