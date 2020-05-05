<properties
    pageTitle="(Preview) Buy SQL DB reserved capacity to save money"
    description="(Preview) Buy SQL DB reserved capacity to save money"
    authors="yashesvi"
    ms.author="yashar"
    articleId="919e7952-0ff9-4cc2-9652-408573da6076_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
    ownershipId="ACE_ReservedInstances"
/>
# Buy SQL DB Reserved capacity to save money over pay-as-you-go costs
---
{
  "recommendationOfferingId": "07649cbd-2ee4-4992-898b-f5f16bad1b36",
  "recommendationOfferingName": "(New) SQL DB vCores Reserved Capacity",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "c6ac1f03-bd58-4421-9522-23cffb64d8e1",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('acereservations.kusto.windows.net').database('reservations').getSQLDBRecoAdvisor()",
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
  "description": "(New) Consider SQL DB reserved capacity to save money over pay-as-you-go costs",
  "longDescription": "Reserved capacity can provide a significant discount over pay-as-you-go prices. With reserved capacity, you can pre-pay for your SQL DB hourly compute costs for a duration of 1 or 3 years. Discounts will automatically apply to new or existing matching deployments. We analyzed your usage over the last 30 days and recommend reserved capacity where we determined savings.",
  "potentialBenefits": "savings",
  "actions": [
    {
      "actionId": "b3a3bbb5-feaf-4c02-9d67-aa314bc1b477",
      "description": "(New) Consider reserved capacity for {sku} in {region} for {qty} vCores",
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
  "tip": "You can buy SQL DB reserved capacity to save money over pay-as-you-go costs.",
  "costSavingInfo": "*You can save up to the stated amount if you purchase single subscription reservations for 3 years and your future usage follows the same pattern as the last 30 days. You actual savings may vary."
}
---
