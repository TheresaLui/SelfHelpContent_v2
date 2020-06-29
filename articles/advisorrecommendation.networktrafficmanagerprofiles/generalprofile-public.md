<properties
    pageTitle="Add at least one more endpoint to the profile, preferably in another Azure region"
    description="Add at least one more endpoint to the profile, preferably in another Azure region"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="6cd70072-c45c-4716-bf7b-b35c18e46e72_Public"
    selfHelpType="advisorRecommendationMetadata"
    productPesIds="15400"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="CloudNet_TrafficManager"
/>
# Add at least one more endpoint to the profile, preferably in another Azure region
---
{
  "recommendationOfferingId": "9264a786-286a-41e2-b8aa-4210461010a4",
  "recommendationOfferingName": "Traffic Manager",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "6cd70072-c45c-4716-bf7b-b35c18e46e72",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "Public.Production.Watm.Advisor.GeneralEndpoints",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Network/trafficmanagerprofiles",
  "recommendationFriendlyName": "GeneralProfile",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "atmredmond@microsoft.com",
    "icm": {
      "routingId": "Metrics://TrafficManager",
      "service": "Cloudnet",
      "team": "TrafficManager"
    },
    "serviceTreeId": "d99081c1-c81f-49e3-8aec-541f00ffba62"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/AA1o0x4",
  "description": "Add at least one more endpoint to the profile, preferably in another Azure region",
  "longDescription": "Profiles should have more than one endpoint to ensure availability if one of the endpoints fails. It is also recommended that endpoints be in different regions.",
  "potentialBenefits": "Improve resiliency by allowing failover",
  "actions": [
    {
      "actionId": "c05c5214-5e3b-45eb-b811-4cd98157b9d4",
      "description": "Add another endpoint for failover",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}",
        "menuid": "endpoints"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "1f5147e8-3437-4537-975b-3d32aae47ae2",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Add Endpoint",
  "additionalColumns": []
}
---
