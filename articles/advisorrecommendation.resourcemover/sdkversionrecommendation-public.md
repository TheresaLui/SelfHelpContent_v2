<properties
    pageTitle="Upgrade SDK version recommendation for Azure Resource Mover"
    description="Return list of resources that do not currently use the recommended SDK version"
    authors="natarajs"
    ms.author="natarajs"
    articleId="703fbf6c-ab3a-47d2-aa26-9092d06a6054_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, ussec, usnat"
    ownershipId="Compute_AzureResourceMover"
/>
# Azure Resource Mover SDK Ugrade Recommendation
---
{
    "$schema": "AdvisorRecommendation",
    "recommendationOfferingId": "804d176b-e45c-409c-91c9-0d87467837fe",
    "recommendationOfferingName": "Resource Move",
    "recommendationTypeId": "703fbf6c-ab3a-47d2-aa26-9092d06a6054",
    "dataSourceMetadata": {
        "schemaVersion": 1.0,
        "streamNamespace": "cluster('https://rmscluswus.kusto.windows.net').database('RMSKustoDB').GetSDKUsersSubscriptionIds_AA_RMS",
        "dataSource": "Kusto",
        "refreshInterval": "1:00:00:00"
    },
    "recommendationCategory": "Performance",
    "recommendationImpact": "Medium",
    "recommendationResourceType": "Microsoft.Subscriptions/subscriptions",
    "recommendationFriendlyName": "UpgradeResourceMoverSDK",
    "recommendationMetadataState": "Disabled",
    "portalFeatures": [],
    "owner": {
        "email": "azregionmove@microsoft.com",
        "icm": {
            "routingId": "MDM://AzRMS",
            "service": "Azure Resource Mover",
            "team": "Azure Resource Mover Engineering Team"
        },
        "serviceTreeId": "dd885aa5-f295-4101-98da-6e7b280660da"
    },
    "ingestionClientIdentities": [],
    "recommendationTimeToLive": 3600,
    "version": 1.1,
    "learnMoreLink": "https://docs.microsoft.com/azure/resource-mover/",
    "description": "Update Azure Resource Mover SDK Version",
    "longDescription": "We have identified that you are using an older version of SDK. The latest version of SDK contains new features such as dependency validation improvements, ability to delete source resources, and portal improvements, in addition to several fixes proactively identified though our QA process.",
    "potentialBenefits": "Latest Azure Resource Mover SDK contains the most recent feature functionality",
    "supportedSDKLanguages": [".Net"],
    "actions": [
        {
            "actionId": "4af17698-a8ed-4d2d-aa95-adcce9fce77e",
            "description": "Learn how to update your Resource Mover SDK ",
            "actionType": "Document",
            "documentLink": "https://www.nuget.org/packages/Microsoft.Azure.Management.Migrate.ResourceMover/"
        }
    ],
    "resourceMetadata": {
        "action": {
            "actionId": "3c032c7d-4cc7-44a0-91d5-91466ba2a4e5",
            "actionType": "Blade",
            "extensionName": "HubsExtension",
            "bladeName": "ResourceMenuBlade",
            "metadata": {
                "id": "{resourceId}"
            }
        }
    },
    "displayLabel": "Update Azure Resource Mover SDK",
    "additionalColumns": []
}
---
