<properties
    pageTitle="Delete ExpressRoute circuits in the provider status of Not Provisioned"
    description="Delete ExpressRoute circuits in the provider status of Not Provisioned"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="da6630fb-4286-4996-92a3-a43f5f26dd34_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Delete ExpressRoute circuits in the provider status of Not Provisioned
---
{
  "recommendationOfferingId": "3e80411f-1930-4048-abf3-235c22b3850a",
  "recommendationOfferingName": "ExpressRoute",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "da6630fb-4286-4996-92a3-a43f5f26dd34",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "AzureAnalytics.Partner.Networking.ExR.ExRNotProvisionedCircuitsForAzureAdvisor_Pub",
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
  "version": 2.0,
  "learnMoreLink": "https://aka.ms/expressroute",
  "description": "Delete ExpressRoute circuits in the provider status of Not Provisioned",
  "longDescription": "We noticed that your ExpressRoute circuit is in the provider status of Not Provisioned for more than one month. This circuit is currently billed hourly to your subscription. We recommend that you delete the circuit if you aren't planning to provision the circuit with your connectivity provider.",
  "potentialBenefits": "Cost savings",
  "actions": [
    {
      "actionId": "dd5b01af-7897-4686-ac02-7d57f1dfbe3f",
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
      "actionId": "0674d32d-c905-4228-9e4f-e42f19252ade",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Network",
      "bladeName": "ExpressRouteBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Delete ExpressRoute circuit in Not Provisioned state",
  "additionalColumns": [],
  "remediation": [
    {
      "httpMethod": "DELETE",
      "uri": "{armEndpoint}{resourceId}?api-version=2019-09-01",
      "actionId": "dd5b01af-7897-4686-ac02-7d57f1dfbe3f",
      "implication": "There is availability implication for this action.",
      "documentationLink": "https://docs.microsoft.com/rest/api/expressroute/expressroutecircuits/delete"
    }
  ]
}
---
