<properties
    pageTitle="(Preview) Buy Database for MariaDB reserved capacity to save"
    description="(Preview) Buy Database for MariaDB reserved capacity to save"
    authors="yashesvi"
    ms.author="yashar"
    articleId="171f87ad-4ead-42fc-8f32-a3b18d451837_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
    ownershipId="ACE_ReservedInstances"
/>
# Buy MySQL DB Reserved capacity to save money over pay-as-you-go costs
---
{
  "recommendationOfferingId": "171f87ad-4ead-42fc-8f32-a3b18d451837",
  "recommendationOfferingName": "ReservedInstances",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "06ad499a-0952-48d3-b061-ec81c9cabb8b",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('acereservations.kusto.windows.net').database('reservations').getMariaDBRecoAdvisor()",
    "dataSource": "Kusto",
    "refreshInterval":"00.12:59:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Subscriptions/subscriptions",
  "recommendationFriendlyName": "MariaDBSQLReservedCapacity",
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
  "description": "(Preview) Consider reserved capacity for Database for MariaDB compute usage and save over your pay-as-you-go costs",
  "longDescription": "We analyzed you MariaDB Database usage pattern over last 30 days and recommend reserved capacity purchase that maximizes your savings. With reserved capacity you can pre-purchase MariaDB hourly usage and save over your compute costs. Reserved capacity is a billing benefit and will automatically apply to new or existing deployments. Saving estimates are calculated for individual subscriptions using 3-year reservation pricing and by extrapolating the usage pattern observed over last 30 days. Shared scope recommendations are available in reservation purchase experience and can increase savings further.",
  "potentialBenefits": "savings",
  "actions": [
    {
      "actionId": "171f87ad-4ead-42fc-8f32-a3b18d451837",
      "description": "(Preview) Consider reserved capacity for {displaySKU} in {displayRegion} for {displayQty} vCores",
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
  "tip": "You can buy Database for MariaDB reserved capacity to save money over pay-as-you-go costs.",
  "costSavingInfo": "*You can save up to the stated amount if you purchase single subscription reservations for 3 years and your future usage follows the same pattern as the last 30 days. You actual savings may vary."
}
---
