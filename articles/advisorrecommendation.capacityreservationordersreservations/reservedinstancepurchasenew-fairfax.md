<properties
    pageTitle="Purchase a new Reserved instance for your expiring Reserved instances"
    description="Purchase a new Reserved instance for your expiring Reserved instances"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="abb1f687-2d58-4197-8f5b-8882f05c04b8_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
/>
# Purchase a new Reserved instance for your expiring Reserved instances
---
{
  "recommendationOfferingId": "07649cbd-2ee4-4992-898b-f5f16bad1b36",
  "recommendationOfferingName": "Virtual Machines",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "abb1f687-2d58-4197-8f5b-8882f05c04b8",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Capacity/reservationOrders/reservations",
  "recommendationFriendlyName": "ReservedInstancePurchaseNew",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "aadevteam@microsoft.com",
    "icm": {
      "routingId": "MDM://AzureAdvisor",
      "service": "Azure Advisor",
      "team": "Azure Advisor"
    },
    "serviceTreeId": "f6d7f416-ee14-4943-894b-1abca9140b74"
  },
  "ingestionClientIdentities": [
    "9711bc82-585b-4a9f-a48b-a035209b7f45"
  ],
  "recommendationTimeToLive": 86400,
  "version": 2.0,
  "learnMoreLink": "https://aka.ms/reservedinstances",
  "description": "Purchase a new Reserved instance for your expiring Reserved instances",
  "longDescription": "Reserved instances listed below are expiring soon or recently expired. Your resources will continue to operate normally, however, you will be billed at the pay-as-you-go rates going forward. To optimize your costs, purchase a replacement for the expiring RIs.",
  "potentialBenefits": "Continue to receive discounted rates for your resources",
  "actions": [
    {
      "actionId": "f04de9c9-5b7d-46c6-8642-5636cae7cb66",
      "description": "Renew",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Reservations",
      "bladeName": "CreateBlade",
      "metadata": {
        "filters": {
          "reservedResourceType": "{ResourceType}",
          "subId": "{subscriptionId}",
          "scope": "{AppliedScopeType}",
          "region": "{Region}",
          "sku": "{SKU}",
          "term": "{Term}",
          "quantity": "{Quantity}"
        },
        "referrer": "AzureAdvisorRiRenewal"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "be042b22-7763-4b09-a87a-d8840b6449da",
      "description": "{ReservationName}",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{ReservationId}",
        "name": "{ReservationName}"
      }
    }
  },
  "displayLabel": "Renew your reserved instances",
  "additionalColumns": [
    {
      "name": "ExpiryDate",
      "title": "Expiry Date"
    },
    {
      "name": "Product",
      "title": "Product"
    },
    {
      "name": "Quantity",
      "title": "Quantity"
    }
  ],
  "tip": "Purchase a new Reserved VM Instance for your expiring RI to continue receiving discounted rates.",
  "costSavingInfo": "*You can save up to the stated amount if you purchase single subscription reservations for 3 years and your future usage follows the same pattern as the last 30 days. Your actual savings may vary."
}
---
