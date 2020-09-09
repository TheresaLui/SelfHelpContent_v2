<properties
    pageTitle="(Preview) Buy SQL PaaS Database reserved capacity to save"
    description="(Preview) Buy SQL PaaS Database reserved capacity to save"
    authors="yashesvi"
    ms.author="yashar"
    articleId="a1d7f3cd-7328-4f0d-8e69-903e9caa4caa_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="ACE_ReservedInstances"
/>
# Buy SQL DB Reserved capacity to save money over pay-as-you-go costs
---
{
  "recommendationOfferingId": "07649cbd-2ee4-4992-898b-f5f16bad1b36",
  "recommendationOfferingName": "ReservedInstances",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "885cd4f5-dfa0-4d68-bbfd-00f89fc2b69c",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('acereservations.kusto.windows.net').database('reservations').getSQLDBRecoAdvisor()",
    "dataSource": "Kusto",
    "refreshInterval":"00.12:10:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Subscriptions/subscriptions",
  "recommendationFriendlyName": "SQLReservedCapacity",
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
  "version": 8.0,
  "learnMoreLink": "https://aka.ms/rirecommendations",
  "description": "(Preview) Consider SQL PaaS DB reserved capacity to save over your pay-as-you-go costs",
  "longDescription": "We analyzed your SQL PaaS usage pattern over last 30 days and recommend reserved capacity purchase that maximizes your savings. With reserved capacity you can pre-purchase hourly usage for your SQL PaaS deployments and save over your SQL PaaS compute costs. SQL license is charged separately and is not discounted by the reservation. Reserved capacity is a billing benefit and will automatically apply to new or existing deployments. Saving estimates are calculated for individual subscriptions using 3-year reservation pricing and the usage pattern observed over last 30 days. Shared scope recommendations are available in reservation purchase experience and can increase savings further.",
  "potentialBenefits": "savings",
  "actions": [
    {
      "actionId": "b3a3bbb5-feaf-4c02-9d67-aa314bc1b477",
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
  "tip": "You can buy SQL PaaS reserved capacity to save money over pay-as-you-go costs.",
  "costSavingInfo": "*You can save up to the stated amount if you purchase single subscription reservations for 3 years and your future usage follows the same pattern as the last 30 days. You actual savings may vary."
}
---
