<properties
    pageTitle="(Preview) Buy Azure App Service isolated plan stamp fee reserved capacity to save"
    description="(Preview) Buy App Service isolated plan stamp fee reserved capacity to save"
    authors="yashesvi"
    ms.author="yashar"
    articleId="5b8ddf04-be28-44ec-ab2c-a63a34d1de13_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
    ownershipId="ACE_ReservedInstances"
/>
# Buy AppService Reserved capacity to save money over pay-as-you-go costs
---
{
  "recommendationOfferingId": "07649cbd-2ee4-4992-898b-f5f16bad1b36",
  "recommendationOfferingName": "ReservedInstances",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "5b8ddf04-be28-44ec-ab2c-a63a34d1de13",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('acereservations.kusto.windows.net').database('reservations').getAppServiceRecoAdvisor()",
    "dataSource": "Kusto",
    "refreshInterval":"00.23:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Subscriptions/subscriptions",
  "recommendationFriendlyName": "AppServiceReservedCapacity",
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
  "version": 6.0,
  "learnMoreLink": "https://aka.ms/rirecommendations",
  "description": "(Preview) Consider App Service stamp fee reserved capacity to save over your on-demand costs",
  "longDescription": "We analyzed you App Service isolated environment stamp fees usage pattern over last 30 days and recommend reserved capacity purchase that maximizes your savings. With reserved capacity you can pre-purchase hourly usage for the isolated environment stamp fee and save over your Pay-as-you-go costs. Note that reserved capacity only applies to the stamp fee and not to the App Service instances.  Reserved capacity is a billing benefit and will automatically apply to new or existing deployments. Saving estimates are calculated for individual subscriptions using 3-year reservation pricing based on usage pattern over last 30 days.",
  "potentialBenefits": "savings",
  "actions": [
    {
      "actionId": "5b8ddf04-be28-44ec-ab2c-a63a34d1de13",
      "description": "(Preview) Consider {displaySKU} reserved capacity in {displayRegion} for {qty} isolated plan stamps",
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
  "tip": "You can buy Azure AppService reserved capacity to save money over pay-as-you-go costs.",
  "costSavingInfo": "*You can save up to the stated amount if you purchase single subscription reservations for 3 years and your future usage follows the same pattern as the last 30 days. You actual savings may vary."
}
---
