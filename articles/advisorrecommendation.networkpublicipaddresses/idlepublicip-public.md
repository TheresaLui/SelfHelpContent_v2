<properties
    pageTitle="Delete Public IP address not associated to a running Azure resource"
    description="Delete Public IP address not associated to a running Azure resource"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="1b4dd958-c202-47af-af97-99bfc98376a5_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Delete Public IP address not associated to a running Azure resource
---
{
  "recommendationOfferingId": "046ee569-27c5-4c9e-b0fc-815701a22ff2",
  "recommendationOfferingName": "Virtual Network",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "1b4dd958-c202-47af-af97-99bfc98376a5",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "AzureAdvisor.IdlePublicIpV2_Public",
    "dataSource": "Cosmos",
    "refreshInterval": "01:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Network/publicIPAddresses",
  "recommendationFriendlyName": "IdlePublicIp",
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
  "version": 5.0,
  "learnMoreLink": "https://aka.ms/aa_idlepublicip_learnmore",
  "description": "Delete Public IP address not associated to a running Azure resource",
  "longDescription": "Public IPs are associated with Azure resources to communicate with the internet. Public IPs can be associated to Azure Virtual Machines, Azure Load Balancers or other resources. These IP addresses come with a nominal charge. If they are not being actively used through association to a running Azure resource, deleting these IP addresses can result in cost saving.",
  "potentialBenefits": "Ensure cost savings by deleting unassociated Public IP addresses",
  "actions": [
    {
      "actionId": "fb603449-7795-4148-ac51-cafcf71430ed",
      "description": "Delete unassociated Public IP addresses",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Network",
      "bladeName": "PublicIpAddressBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "fd7592d8-ba86-4a49-8b8c-526cbc832838",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "remediation": [
    {
      "httpMethod": "DELETE",
      "uri": "{armEndpoint}{resourceId}?api-version=2019-09-01",
      "actionId": "fb603449-7795-4148-ac51-cafcf71430ed",
      "implication": "There is availability implication for this action.",
      "documentationLink": "https://docs.microsoft.com/rest/api/virtualnetwork/publicipaddresses/delete"
    }
  ],
  "displayLabel": "Delete unassociated Public IPs",
  "additionalColumns": [],
  "tip": "You can delete your unassociated public IP address to reduce your monthly Azure spend.",
  "costSavingInfo": "*You can save up to the stated amount if you choose to delete the public IP address. Your actual savings may vary."
}
---
