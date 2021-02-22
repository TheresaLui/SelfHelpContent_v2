<properties
pageTitle = "Implement multiple ExpressRoute circuits in your Virtual Network for cross premises resiliency"
description = "Implement multiple ExpressRoute circuits in your Virtual Network for cross premises resiliency"
authors = "aadevteam"
ms.author = "aadevteam"
articleId = "79319e4d-f4ba-4c45-bdcf-4df91a56598a_Fairfax"
selfHelpType = "advisorRecommendationMetadata"
cloudEnvironments = "Fairfax" 
	ownershipId="CloudNet_AzureExpressRoute"
/>
# Implement multiple ExpressRoute circuits in your Virtual Network for cross premises resiliency
---
{
    "recommendationOfferingId": "7269b88e-b638-4ba5-a55e-5632365dd938",
    "recommendationOfferingName": "ExpressRoute",
    "$schema": "AdvisorRecommendation",
    "recommendationTypeId": "70f87e66-9b2d-4bfa-ae38-1d7d74837689",
    "dataSourceMetadata": {
        "schemaVersion": 1.0,
        "streamNamespace": "Microsoft.Cloud.AzureAdvisorSingleCircuit-FF",
        "dataSource": "Cosmos",
        "refreshInterval": "1.00:00:00"
    },
    "recommendationCategory": "HighAvailability",
    "recommendationImpact": "Medium",
    "recommendationResourceType": "Microsoft.Network/virtualNetworkGateways",
    "recommendationFriendlyName": "ExpressRouteGatewayRedundancy",
    "recommendationMetadataState": "Active",
    "portalFeatures": [],
    "owner": {
        "email": "ExRPM@microsoft.com",
        "icm": {
            "routingId": "AIMS://ExpressRoute",
            "service": "Cloudnet",
            "team": "ExpressRoute"
        },
        "serviceTreeId": "7269b88e-b638-4ba5-a55e-5632365dd938"
    },
    "ingestionClientIdentities": [],
    "recommendationTimeToLive": 86400,
    "version": 1.0,
    "learnMoreLink": "https://docs.microsoft.com/azure/expressroute/designing-for-high-availability-with-expressroute",
    "description": "Implement multiple ExpressRoute circuits in your Virtual Network for cross premises resiliency",
    "longDescription": "We have detected that your ExpressRoute gateway only has 1 ExpressRoute circuit associated to it. Connect 1 or more additional circuits to your gateway to ensure peering location redundancy and resiliency",
    "potentialBenefits": "Improve resiliency in case of ExpressRoute peering location failure",
    "actions": [{
        "actionId": "3fed8ea6-8495-4d5c-a5a0-2ea656d2c8e4",
        "description": "Link additional circuits to your ExpressRoute Gateway",
        "actionType": "Document",
        "documentLink": "https://docs.microsoft.com/azure/expressroute/expressroute-howto-linkvnet-portal-resource-manager"
    }],
    "resourceMetadata": {
        "action": {
            "actionId": "50f99694-9ea2-4cfa-a6a6-e1e25eb57ebf",
            "actionType": "Blade",
            "extensionName": "Microsoft_Azure_Network",
            "bladeName": "VirtualNetworkGatewayBlade",
            "metadata": {
                "id": "{resourceId}"
            }
        }
    },
    "displayLabel": "Implement multiple ExpressRoute circuits in your Virtual Network for cross premises resiliency",
    "additionalColumns": []
}
---
