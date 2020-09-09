<properties
    pageTitle="(Preview) Buy Database for MariaDB reserved capacity to save"
    description="(Preview) Buy Database for MariaDB reserved capacity to save"
    authors="yashesvi"
    ms.author="yashar"
    articleId="8ee30d6b-2c73-452a-b4ad-e4386cd6f7d0_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
    ownershipId="ACE_ReservedInstances"
/>
# Buy Redis Cache Reserved capacity to save money over pay-as-you-go costs
---
{
  "recommendationOfferingId": "07649cbd-2ee4-4992-898b-f5f16bad1b36",
  "recommendationOfferingName": "ReservedInstances",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "8ee30d6b-2c73-452a-b4ad-e4386cd6f7d0",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('acereservations.kusto.windows.net').database('reservations').getRedisCacheRecoAdvisor()",
    "dataSource": "Kusto",
    "refreshInterval":"00.13:10:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Subscriptions/subscriptions",
  "recommendationFriendlyName": "RedisCacheReservedCapacity",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "cabri@microsoft.com",
    "icm": {
      "routingId": "CABRI://ReservationsCore",
      "service": "Reservations RP",
      "team": "Reservations Core"
    },
    "serviceTreeId": "d69e4730-c500-4755-a0be-dbe134ba7dbb"
  },
  "recommendationTimeToLive": 86400,
  "version": 2.0,
  "learnMoreLink": "https://aka.ms/rirecommendations",
  "description": "(Preview) Consider Cache for Redis reserved capacity to save over your pay-as-you-go costs",
  "longDescription": "We analyzed you Cache for Redis usage pattern over last 30 days and calculated reserved capacity purchase that maximizes your savings. With reserved capacity you can pre-purchase Cache for Redis hourly usage and save over your current on-demand costs. Reserved capacity is a billing benefit and will automatically apply to new or existing deployments. Saving estimates are calculated for individual subscriptions using 3-year reservation pricing and the usage pattern observed over last 30 days. Shared scope recommendations are available in reservation purchase experience and can increase savings further.",
  "potentialBenefits": "savings",
  "actions": [
    {
      "actionId": "8ee30d6b-2c73-452a-b4ad-e4386cd6f7d0",
      "description": "(Preview) Consider reserved capacity for {displaySKU} in {displayRegion} for {displayQty} nodes",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Reservations",
      "bladeName": "CreateBlade",
      "metadata": {
        "filters": {
          "reservedResourceType": "{reservedResourceType}",
          "subId": "{subscriptionId}",
          "scope": "{scope}",
          "sku": "{sku}",
          "region": "{region}",
          "term": "{term}"
        },
        "referrer": "AzureAdvisor"
      }
    }
  ],
  "displayLabel": "Buy reserved capacity",
  "tip": "You can buy Cache for Redis reserved capacity and save money over on-demand costs.",
  "costSavingInfo": "*You can save up to the stated amount if you purchase single subscription reservations for 3 years and your future usage follows the same pattern as the last 30 days. You actual savings may vary."
}
---
