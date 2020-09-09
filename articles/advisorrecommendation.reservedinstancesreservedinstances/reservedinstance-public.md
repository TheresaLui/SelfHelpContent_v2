<properties
    pageTitle="Buy virtual machine reserved instances to save money over pay-as-you-go costs"
    description="Buy virtual machine reserved instances to save money over pay-as-you-go costs"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="84b1a508-fc21-49da-979e-96894f1665df_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="RedisCache_RedisCache"
/>
# Buy virtual machine reserved instances to save money over pay-as-you-go costs
---
{
  "recommendationOfferingId": "07649cbd-2ee4-4992-898b-f5f16bad1b36",
  "recommendationOfferingName": "ReservedInstances",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "84b1a508-fc21-49da-979e-96894f1665df",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.ReservedInstances/reservedInstances",
  "recommendationFriendlyName": "ReservedInstance",
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
    "414f602c-67a0-40de-98f7-fbc02bbda8b1",
    "19c2f118-ef78-4dcb-83eb-d715c67d8c39",
    "97d24591-f8f4-457f-9b3d-896eb4d414a4"
  ],
  "recommendationTimeToLive": 86400,
  "version": 2.0,
  "learnMoreLink": "https://aka.ms/reservedinstances",
  "description": "Buy virtual machine reserved instances to save money over pay-as-you-go costs",
  "longDescription": "Reserved instances can provide a significant discount over pay-as-you-go prices. With reserved instances, you can pre-purchase the base costs for your virtual machines. Discounts will automatically apply to new or existing VMs that have the same size and region as your reserved instance. We analyzed your usage over the last 30 days and recommend money-saving reserved instances.",
  "potentialBenefits": "savings",
  "actions": [
    {
      "actionId": "b3a3bbb5-feaf-4c02-9d67-aa314bc1b477",
      "description": "Buy reserved instances to save over pay-as-you-go costs",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Reservations",
      "bladeName": "CreateBlade",
      "metadata": {
        "filters": {
          "reservedResourceType": "VirtualMachines",
          "subId": "{subscriptionId}",
          "scope": "{scope}",
          "region": "{location}",
          "sku": "{vmSize}",
          "term": "{term}",
          "quantity": "{targetResourceCount}"
        },
        "referrer": "AzureAdvisor"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "d652c8e4-a4d1-4a6b-afd8-a5430c9bd963",
      "description": "{vmSize} virtual machines in {location}",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Expert",
      "bladeName": "ReservedInstanceDetailsBlade",
      "metadata": {
        "subscriptionId": "{subscriptionId}",
        "vmSize": "{vmSize}",
        "location": "{location}",
        "quantity": "{targetResourceCount}"
      }
    }
  },
  "displayLabel": "Buy reserved instances",
  "additionalColumns": [
    {
      "name": "targetResourceCount",
      "title": "Recommended Quantity"
    }
  ],
  "tip": "You can buy virtual machine reserved instances to save money over pay-as-you-go costs.",
  "costSavingInfo": "*You can save up to the stated amount if you purchase single subscription reservations for 3 years and your future usage follows the same pattern as the last 30 days. Your actual savings may vary."
}
---
