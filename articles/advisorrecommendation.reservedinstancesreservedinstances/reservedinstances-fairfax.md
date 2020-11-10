<properties
    pageTitle="Buy virtual machine reserved instances to save money over pay-as-you-go costs"
    description="Buy virtual machine reserved instances to save money over pay-as-you-go costs"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="84b1a508-fc21-49da-979e-96894f1665df_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="ACE_ReservedInstances"
/>
# Buy virtual machine reserved instances to save money over pay-as-you-go costs
---
{
   "recommendationOfferingId":"07649cbd-2ee4-4992-898b-f5f16bad1b36",
   "recommendationOfferingName":"ReservedInstances",
   "$schema":"AdvisorRecommendation",
   "recommendationTypeId":"84b1a508-fc21-49da-979e-96894f1665df",
   "dataSourceMetadata":{
      "streamNamespace":"",
      "dataSource":"SAS"
   },
   "recommendationCategory":"Cost",
   "recommendationImpact":"High",
   "recommendationResourceType":"Microsoft.ReservedInstances/reservedInstances",
   "recommendationFriendlyName":"ReservedInstance",
   "recommendationMetadataState":"Active",
   "owner":{
    "email": "aipuaedevs@microsoft.com",
    "icm": {
        "routingId": "routetoUAEteam",
        "service": "Usage Alllocation Engine",
        "team": "UAE"
    },
    "serviceTreeId": "fb1567ae-acf8-42c9-9fd4-0a757d7c2983"
   },
   "ingestionClientIdentities":[
      "CN=usage-services-identity-prod.usage.microsoft.com"
   ],
   "version":1.0,
   "learnMoreLink":"https://aka.ms/reservedinstances",
   "description":"Buy virtual machine reserved instances to save money over pay-as-you-go costs",
   "longDescription": "Reserved instances can provide a significant discount over pay-as-you-go prices. With reserved instances, you can pre-purchase the base costs for your virtual machines. Discounts will automatically apply to new or existing VMs that have the same size and region as your reserved instance. We analyzed your usage over the last 30 days and recommend money-saving reserved instances.",
   "potentialBenefits": "savings",
   "actions":[
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
        },
         "documentLink":""
      }
   ],
   "resourceMetadata":{
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
   "displayLabel":"Buy reserved instances",
   "additionalColumns":[
    {
        "name": "targetResourceCount",
        "title": "Recommended Quantity"
    }
   ],
   "tip": "You can buy virtual machine reserved instances to save money over pay-as-you-go costs.",
   "costSavingInfo": "*You can save up to the stated amount if you purchase single subscription reservations for 3 years and your future usage follows the same pattern as the last 30 days. Your actual savings may vary."
}
---
