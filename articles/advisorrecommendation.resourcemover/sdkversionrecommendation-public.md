<properties
    pageTitle="Upgrade SDK version recommendation"
    description="Return list of resources that do not currently use the recommended SDK version"
    ms.author="natarajs"
    articleId="703fbf6c-ab3a-47d2-aa26-9092d06a6054_public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="public,usnat,ussec"
    ownershipId="Compute_AzureResourceMover"
/>
# Resource Mover SDK Ugrade Recommendation
---
{ 
    "recommendationOfferingId": "804d176b-e45c-409c-91c9-0d87467837fe", 
    "recommendationOfferingName": "Resource Move", 
    "$schema": "AdvisorRecommendation", 
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
    "recommendationMetadataState": "Active", 
    "portalFeatures": [], 
    "owner": { 
        "email": "azregionmove@microsoft.com", 
        "icm": { 
            "routingId": "mdm://adspartner", 
            "service": "AzureResourceMover", 
            "team": "AzureResourceMoverEngineeringTeam" 
        }, 
        "serviceTreeId": "dd885aa5-f295-4101-98da-6e7b280660da" 
    }, 
    "ingestionClientIdentities": [], 
    "recommendationTimeToLive": 86400, 
    "version": 1.0, 
    "learnMoreLink": "https://docs.microsoft.com/azure/resource-mover/", 
    "description": "Update Azure Resource Mover SDK Version", 
    "longDescription": "Provide this data", 
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
    "testData": "e80eb9fa-c996-4435-aa32-5af6f3d3077c,/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c"
}
---
