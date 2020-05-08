<properties
    pageTitle="(Preview) Buy Cosmos DB reserved capacity to save over your pay-as-you-go costs"
    description="(Preview) Buy Cosmos DB reserved capacity to save over your pay-as-you-go costs"
    authors="yashesvi"
    ms.author="yashar"
    articleId="a205074f-8049-48b3-903f-556f5e530ae3_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
    ownershipId="ACE_ReservedInstances"
/>
# Buy Cosmos DB Reserved capacity to save money over pay-as-you-go costs
---
{
  "recommendationOfferingId": "07649cbd-2ee4-4992-898b-f5f16bad1b36",
  "recommendationOfferingName": "(Preview) Cosmos DB Reserved Capacity",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "a205074f-8049-48b3-903f-556f5e530ae3",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('acereservations.kusto.windows.net').database('reservations').getCosmosRecoAdvisor()",
    "dataSource": "Kusto",
    "refreshInterval":"00.00:10:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Subscriptions/subscriptions",
  "recommendationFriendlyName": "CosmosDBReservedCapacity",
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
  "version": 4.0,
  "learnMoreLink": "https://aka.ms/rirecommendations",
  "description": "(Preview) Consider Cosmos DB reserved capacity to save over your pay-as-you-go costs",
  "longDescription": "We analyzed your Cosmos DB usage pattern over last 30 days and recommend reserved capacity purchase to optimize costs. With reserved capacity you can pre-purchase Cosmos DB hourly usage and save over your pay-as-you-go costs. Reserved capacity is a billing benefit and will automatically apply to new or existing deployments. Saving estimates are calculated for individual subscriptions using 3-year reservation pricing and by extrapolating the usage pattern observed over last 30 days. Shared scope recommendations are available in reservation purchase experience and can increase savings even more.",
  "potentialBenefits": "savings",
  "actions": [
    {
      "actionId": "b3a3bbb5-feaf-4c02-9d67-aa314bc1b477",
      "description": "(Preview) Consider purchasing {displaySKU} reserved capacity",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Reservations",
      "bladeName": "CreateBlade",
      "metadata": {
        "filters": {
          "reservedResourceType": "{reservedResourceType}",
          "subId": "{subscriptionId}",
          "scope": "{scope}",
          "sku": "{sku}",
          "term": "{term}"
        },
        "referrer": "AzureAdvisor"
      }
    }
  ],
  "displayLabel": "Buy reserved capacity",
  "tip": "You can buy Cosmos DB reserved capacity to save money over pay-as-you-go costs.",
  "testData": "73c0021f-a37d-433f-8baa-7450cb54eea6,/subscriptions/73c0021f-a37d-433f-8baa-7450cb54eea6,\"{\"\"reservedResourceType\"\":\"\"CosmosDb\"\",\"\"term\"\":\"\"P3Y\"\",\"\"subId\"\":\"\"73c0021f-a37d-433f-8baa-7450cb54eea6\"\",\"\"scope\"\":\"\"Single\"\",\"\"sku\"\":\"\"Cosmos_DB_10000_RUs\"\"}\"",
  "costSavingInfo": "*You can save up to the stated amount if you purchase single subscription reservations for 3 years and your future usage follows the same pattern as the last 30 days. You actual savings may vary."
}
---
