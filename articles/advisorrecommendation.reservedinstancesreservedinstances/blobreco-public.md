<properties
    pageTitle="(Preview) Buy Azure storage reserved capacity to save"
    description="(Preview) Buy Blob storage reserved capacity to save on Blob v2 and and Datalake storage Gen 2"
    authors="yashesvi"
    ms.author="yashar"
    articleId="0169a2e1-c7bf-4c37-90b8-0714811c82d3_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
    ownershipId="ACE_ReservedInstances"
/>
# Buy Blob Reserved capacity to save money over pay-as-you-go costs
---
{
  "recommendationOfferingId": "07649cbd-2ee4-4992-898b-f5f16bad1b36",
  "recommendationOfferingName": "ReservedInstances",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "0169a2e1-c7bf-4c37-90b8-0714811c82d3",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('acereservations.kusto.windows.net').database('reservations').getBlobRecoAdvisor()",
    "dataSource": "Kusto",
    "refreshInterval":"00.14:10:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Subscriptions/subscriptions",
  "recommendationFriendlyName": "BlobReservedCapacity",
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
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/rirecommendations",
  "description": "(Preview) Consider Blob storage reserved capacity to save on Blob v2 and and Datalake storage Gen2 costs",
  "longDescription": "We analyzed you Azure Blob and Datalake storage usage over last 30 days and calculated reserved capacity purchase that would maximize your savings. With reserved capacity you can pre-purchase hourly usage and save over your current on-demand costs. Blob storage reserved capacity applies only to data stored on Azure Blob (GPv2) and Azure Data Lake Storage (Gen 2). Reserved capacity is a billing benefit and will automatically apply to new or existing deployments. Saving estimates are calculated for individual subscriptions using 3-year reservation pricing and the usage pattern observed over last 30 days. Shared scope recommendations are available in reservation purchase experience and can increase savings further.",
  "potentialBenefits": "savings",
  "actions": [
    {
      "actionId": "0169a2e1-c7bf-4c37-90b8-0714811c82d3",
      "description": "(Preview) Consider reserved capacity for {displaySKU} in {displayRegion} for {displayQty}",
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
  "tip": "You can buy Blob storage Gen 2 reserved capacity and save money over on-demand costs.",
  "costSavingInfo": "*You can save up to the stated amount if you purchase single subscription reservations for 3 years and your future usage follows the same pattern as the last 30 days. You actual savings may vary."
}
---
