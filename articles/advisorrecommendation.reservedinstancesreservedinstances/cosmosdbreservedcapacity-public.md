<properties
    pageTitle="(Preview) Buy Cosmos DB reserved capacity to save money"
    description="(Preview) Buy Cosmos DB reserved capacity to save money"
    authors="yashesvi"
    ms.author="yashar"
    articleId="3a5c987a-05f1-44e3-9989-50318e037c5a_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
    ownershipId="RedisCache_RedisCache"
/>
# Buy Cosmos DB Reserved capacity to save money over pay-as-you-go costs
---
{
  "recommendationOfferingId": "07649cbd-2ee4-4992-898b-f5f16bad1b36",
  "recommendationOfferingName": "(Preview) Cosmos DB Reserved Capacity",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "3a5c987a-05f1-44e3-9989-50318e037c5a",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('acereservations.kusto.windows.net').database('reservations').getCosmosRecoAdvisor()",
    "dataSource": "Kusto",
    "refreshInterval":"1.00:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.ReservedInstances/reservedInstances",
  "recommendationFriendlyName": "ReservedCapacity",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "aadevteam@microsoft.com",
    "icm": {
      "routingId": "CABRI://ReservationsCore",
      "service": "Reservations RP",
      "team": "Reservations Core"
    },
    "serviceTreeId": "d69e4730-c500-4755-a0be-dbe134ba7dbb"
  },
  "ingestionClientIdentities": [
    "414f602c-67a0-40de-98f7-fbc02bbda8b1",
    "19c2f118-ef78-4dcb-83eb-d715c67d8c39"
  ],
  "recommendationTimeToLive": 86400,
  "version": 2.0,
  "learnMoreLink": "https://aka.ms/reservedinstances",
  "description": "(Preview) Consider Cosmos DB reserved capacity to save money over pay-as-you-go costs",
  "longDescription": "Reserved capacity can provide a significant discount over pay-as-you-go prices. With reserved capacity, you can pre-purchase your Cosmos DB hourly usage for a duration of 1 or 3 years. Discounts will automatically apply to new or existing matching deployments. We analyzed your usage over the last 30 days and recommend reserved capacity where we determined savings.",
  "potentialBenefits": "savings",
  "actions": [
    {
      "actionId": "b3a3bbb5-feaf-4c02-9d67-aa314bc1b477",
      "description": "Consider {sku} reserved capacity",
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
