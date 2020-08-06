<properties
    pageTitle="Upgrade your SKU or add more instances to ensure fault tolerance"
    description="Upgrade your SKU or add more instances to ensure fault tolerance"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="6a2b1e70-bd4c-4163-86de-5243d7ac05ee_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="CloudNet_AzureApplicationGateway"
/>
# Upgrade your SKU or add more instances to ensure fault tolerance
---
{
  "recommendationOfferingId": "147cf5b4-71a8-4b87-99aa-b444f4a5b51a",
  "recommendationOfferingName": "Application Gateway",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "6a2b1e70-bd4c-4163-86de-5243d7ac05ee",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "azureadvisor.appgatewaysmallorsinglev3_fairfax",
    "dataSource": "Cosmos",
    "refreshInterval": "01:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Network/applicationGateways",
  "recommendationFriendlyName": "AppGateway",
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
  "learnMoreLink": "https://aka.ms/aa_gatewayrec_learnmore",
  "description": "Upgrade your SKU or add more instances to ensure fault tolerance",
  "longDescription": "Deploying two or more medium or large sized instances will ensure business continuity during outages caused by planned or unplanned maintenance.",
  "potentialBenefits": "Ensure business continuity through application gateway resilience",
  "actions": [
    {
      "actionId": "b4f99ca1-da88-408a-bbee-4257964ec259",
      "actionType": "Blade",
      "description": "Upgrade the SKU size",
      "extensionName": "Microsoft_Azure_Network",
      "bladeName": "ApplicationGatewayConfigurationBlade",
      "metadata": {
        "id": "{resourceId}"
      },
      "condition": "applicationGatewayActionType == \"2\""
    },
    {
      "actionId": "e0b4d800-09e0-4aaa-925e-02c8f5fdfdf4",
      "actionType": "Blade",
      "description": "Increase the instance count",
      "extensionName": "Microsoft_Azure_Network",
      "bladeName": "ApplicationGatewayConfigurationBlade",
      "metadata": {
        "id": "{resourceId}"
      },
      "condition": "applicationGatewayActionType == \"3\""
    },
    {
      "actionId": "118b2801-008e-461a-bf6e-078820b4159a",
      "actionType": "Blade",
      "description": "Upgrade the SKU size, and increase the instance count",
      "extensionName": "Microsoft_Azure_Network",
      "bladeName": "ApplicationGatewayConfigurationBlade",
      "metadata": {
        "id": "{resourceId}"
      },
      "condition": "applicationGatewayActionType == \"1\""
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "b614d6a4-27ad-4333-9ac9-e9ef2920fd74",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Upgrade gateway size or add more instances",
  "additionalColumns": [],
  "legacyDataLoader": {
    "className": "Microsoft.Azure.Advisor.Common.DataLoaders.AppGatewayResourceDataParser",
    "assemblyName": "Microsoft.Azure.Advisor.Common"
  }
}
---
