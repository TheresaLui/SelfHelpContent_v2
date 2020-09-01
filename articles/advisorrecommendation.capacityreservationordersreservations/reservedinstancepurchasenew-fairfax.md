<properties
    pageTitle="Configure automatic renewal for your expiring reservations"
    description="Configure automatic renewal for your expiring reservations"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="abb1f687-2d58-4197-8f5b-8882f05c04b8_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="ACE_ReservedInstances"
/>
# Configure auto-renewal for your expiring reservation(s)
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
  "description": "Configure automatic renewal for your expiring reservation",
  "longDescription": "Reserved instances listed below are expiring soon or recently expired. Your resources will continue to operate normally, however, you will be billed at the on-demand rates going forward. To optimize your costs, configure automatic renewal for these reservations or purchase a replacement manually.",
  "potentialBenefits": "Continue to receive discounted rates for your resources",
  "actions": [
    {
      "actionId": "f04de9c9-5b7d-46c6-8642-5636cae7cb66",
      "description": "Renew",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{ReservationId}",
        "menuid": "renewal",
        "referrerInfo": "AdvisorRenewal"
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
  "tip": "Configure auto-renawal for your expiring reservations to continue receiving discounted rates.",
  "testData": "f47a95eb-2112-4234-80d7-1d3d55225cea,/subscriptions/f47a95eb-2112-4234-80d7-1d3d55225cea,\"{\"\"ReservationName\"\":\"\"Test Reservation\"\", \"\"ReservationId\"\": \"\"/providers/microsoft.capacity/reservationOrders/e2e0504f-b8b5-4d79-bd2e-439e2895a366/reservations/f0af5ff9-d18d-4c27-acd3-0225c1023a08\"\",\"\"ExpiryDate\"\":\"\"8/12/2019 12:48:17 AM\"\",\"\"Product\"\":\"\"Test product\"\",\"\"Quantity\"\":\"\"5\"\"}\"",
  "costSavingInfo": "*You can save up to the stated amount if you purchase single subscription reservations for 3 years and your future usage follows the same pattern as the last 30 days. Your actual savings may vary."
}
---
