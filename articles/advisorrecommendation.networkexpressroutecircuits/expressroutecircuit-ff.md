<properties
    pageTitle="Delete ExpressRoute circuits in the provider status of Not Provisioned"
    description="Delete ExpressRoute circuits in the provider status of Not Provisioned"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="3c18c7f0-39d9-4acf-baa1-6387251cf9b4_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Delete ExpressRoute circuits in the provider status of Not Provisioned
---
{
  "recommendationOfferingId": "3e80411f-1930-4048-abf3-235c22b3850a",
  "recommendationOfferingName": "ExpressRoute",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "3c18c7f0-39d9-4acf-baa1-6387251cf9b4",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
        "streamNamespace": "Microsoft.Cloud.AzureAdvisorNotProvisoned-FF",
        "dataSource": "Cosmos",
        "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Network/expressRouteCircuits",
  "recommendationFriendlyName": "ExpressRouteCircuit",
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
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/expressroute",
  "description": "Delete ExpressRoute circuits in the provider status of Not Provisioned",
  "longDescription": "We noticed that your ExpressRoute circuit is in the provider status of Not Provisioned for more than one month. This circuit is currently billed hourly to your subscription. We recommend that you delete the circuit if you aren't planning to provision the circuit with your connectivity provider.",
  "potentialBenefits": "Cost savings",
  "actions": [
    {
      "actionId": "0de4bff0-9349-44ea-8454-0ade22d6089a",
      "description": "Delete ExpressRoute circuit",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Network",
      "bladeName": "ExpressRouteBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "0d001c4f-fcaa-4dca-8c6c-52b7aa5623af",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Network",
      "bladeName": "ExpressRouteBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Delete ExpressRoute circuit in Not Provisioned state",
  "additionalColumns": []
}
---
