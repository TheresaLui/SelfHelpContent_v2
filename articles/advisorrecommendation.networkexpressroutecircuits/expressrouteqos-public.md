<properties
    pageTitle="Upgrade your ExpressRoute circuit bandwidth"
    description="Upgrade your ExpressRoute circuit bandwidth"
    ms.author="ExRPM"
    articleId="f606607c-ee34-445e-997e-49d7cb563fe0_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, USSec, USNat"
    ownershipId="CloudNet_AzureExpressRoute"
/>
# "Upgrade your ExpressRoute circuit bandwidth to accommodate your bandwidth needs"
---
{
  "recommendationOfferingId": "7269b88e-b638-4ba5-a55e-5632365dd938",
  "recommendationOfferingName": "ExpressRoute",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "f606607c-ee34-445e-997e-49d7cb563fe0",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://hybridnetworking.kusto.windows.net').database('aznwmds').f_ER_GetOversubscribingCircuits",
    "dataSource": "Kusto",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Network/expressRouteCircuits",
  "recommendationFriendlyName": "UpgradeERCircuitBandwidth",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "ExRPM@microsoft.com",
    "icm": {
      "routingId": "MDM://AzureExpressRoute",
      "service": "Cloudnet",
      "team": "ExpressRoute"
    },
    "serviceTreeId": "7269b88e-b638-4ba5-a55e-5632365dd938"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1,
  "learnMoreLink": "https://docs.microsoft.com/azure/expressroute/about-upgrade-circuit-bandwidth",
  "description": "Upgrade your ExpressRoute circuit bandwidth to accommodate your bandwidth needs",
  "longDescription": "You have been using over 90% of your procured circuit bandwidth recently. If you exceed your allocated bandwidth, you will experience an increase in dropped packets sent over ExpressRoute. Upgrade your circuit bandwidth to maintain performance if your bandwidth needs remain this high.",
  "potentialBenefits": "Prevent packet drops caused by bandwidth oversubscription",
  "actions": [
    {
      "actionId": "4983f181-0a2a-495a-b5c2-2b580932b487",
      "description": "Upgrade your ExpressRoute circuit bandwidth",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/expressroute/about-upgrade-circuit-bandwidth"
    }
  ],
  "displayLabel": "Upgrade your ExpressRoute circuit bandwidth",
  "additionalColumns": []
}
---
