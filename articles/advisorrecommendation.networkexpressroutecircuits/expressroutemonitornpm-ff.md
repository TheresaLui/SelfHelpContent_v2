<properties
pageTitle = "Implement ExpressRoute Monitor on Network Performance Monitor for end-to-end monitoring of your ExpressRoute circuit"
description = "Implement ExpressRoute Monitor on Network Performance Monitor for end-to-end monitoring of your ExpressRoute circuit"
authors = "aadevteam"
ms.author = "aadevteam"
articleId = "827897c6-2aea-4447-b813-ae363f24218a_Fairfax"
selfHelpType = "advisorRecommendationMetadata"
cloudEnvironments = "Fairfax" 
	ownershipId="CloudNet_AzureExpressRoute"
/>
# "Implement ExpressRoute Monitor on Network Performance Monitor for end-to-end monitoring of your ExpressRoute circuit"
---
{
    "recommendationOfferingId": "7269b88e-b638-4ba5-a55e-5632365dd938",
    "recommendationOfferingName": "ExpressRoute",
    "$schema": "AdvisorRecommendation",
    "recommendationTypeId": "17454550-1543-4068-bdaf-f3ed7cdd3d86",
    "dataSourceMetadata": {
        "schemaVersion": 1.0,
        "streamNamespace": "Microsoft.Cloud.AzureAdvisorExRNpm-FF",
        "dataSource": "Cosmos",
        "refreshInterval": "1.00:00:00"
    },
    "recommendationCategory": "HighAvailability",
    "recommendationImpact": "Medium",
    "recommendationResourceType": "Microsoft.Network/expressRouteCircuits",
    "recommendationFriendlyName": "ExpressRouteGatewayE2EMonitoring",
    "recommendationMetadataState": "Active",
    "portalFeatures": [],
    "owner": {
        "email": "ExRPM@microsoft.com",
        "icm": {
            "routingId": "MDM://AzureAdvisor",
            "service": "Cloudnet",
            "team": "ExpressRoute"
        },
        "serviceTreeId": "7269b88e-b638-4ba5-a55e-5632365dd938"
    },
    "ingestionClientIdentities": [],
    "recommendationTimeToLive": 86400,
    "version": 1.0,
    "learnMoreLink": "https://docs.microsoft.com/azure/expressroute/how-to-npm",
    "description": "Implement ExpressRoute Monitor on Network Performance Monitor for end-to-end monitoring of your ExpressRoute circuit",
    "longDescription": "We have detected that your ExpressRoute circuit is not currently being monitored by ExpressRoute Monitor on Network Performance Monitor. ExpressRoute monitor provides end-to-end monitoring capabilities including: Loss, latency, and performance from on-premises to Azure and Azure to on-premises",
    "potentialBenefits": "Improve time-to-detect and time-to-mitigate issues in your network and provide insights on your network path via ExpressRoute",
    "actions": [{
        "actionId": "cb5fdef6-470d-4e03-a362-ff741e13b084",
        "description": "Configure ExpressRoute Monitor on NPM",
        "actionType": "Document",
        "documentLink": "https://docs.microsoft.com/azure/expressroute/how-to-npm"
    }],
    "resourceMetadata": {
        "action": {
            "actionId": "1f626f4e-53be-4944-a15a-53317a99947b",
            "actionType": "Blade",
            "extensionName": "Microsoft_Azure_Network",
            "bladeName": "ExpressRouteTemplateBlade",
            "metadata": {
                "id": "{resourceId}"
            }
        }
    },
    "displayLabel": "Implement ExpressRoute Monitor on Network Performance Monitor for end-to-end monitoring of your ExpressRoute circuit",
    "additionalColumns": []
}
---
