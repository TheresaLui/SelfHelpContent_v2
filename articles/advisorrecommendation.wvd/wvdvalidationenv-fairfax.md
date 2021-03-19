<properties
    pageTitle="Join validation environment to ensure functionality across service deployments"
    description="Join validation environment to ensure functionality across service deployments"
    authors="marius"
    ms.author="rdinfra"
    articleId="ba1f4576-9ace-4fa9-b0d6-311ad9f2f233_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="Windows_Virtual_Desktop"
/>
# Enable Validation Environment
---
{
  "recommendationOfferingId": "1132b618-fefe-40a0-9256-e685ff575ac7",
  "recommendationOfferingName": "Windows Virtual Desktop",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "ba1f4576-9ace-4fa9-b0d6-311ad9f2f233",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://rdsffx.usgovvirginia.kusto.usgovcloudapi.net').database('WVD').SubscriptionNeedsValidationEnv",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DesktopVirtualization/hostpools",
  "recommendationFriendlyName": "ValidationEnvHostPools",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "rdinfra@microsoft.com",
    "icm": {
      "routingId": "mdm://adspartner/VirtualDesktop",
      "service": "Windows Virtual Desktop",
      "team": "Windows Virtual Desktop"
    },
    "serviceTreeId": "362c0db7-c08b-4471-93ef-c90effc930dd"
  },
  "ingestionClientIdentities": [],
  "version": 1.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/virtual-desktop/create-validation-host-pool",
  "description": "No validation environment enabled",
  "longDescription": "We have determined that you do not have a validation environment enabled in current subscription. When creating your host pools, you have selected \"No\" for \"Validation environment\" in the properties tab. Having at least one host pool with a validation environment enabled ensures the business continuity through Windows Virtual Desktop service deployments with early detection of potential issues.",
  "potentialBenefits": "Ensure business continuity through WVD service deployments",
  "actions": [
    {
      "actionId": "687ba1d6-10e7-4e94-9f90-6d5d5da8d541",
      "description": "Deploy Host Pool to validation environment",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_WVD",
      "bladeName": "WvdManagerMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "0b1afcd0-7b40-47d8-9ae9-ff3e1474bfef",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_WVD",
      "bladeName": "WvdManagerMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Deploy Host Pool to validation environment",
  "additionalColumns": [
    {
      "name": "validationPools",
      "title": "# Validation Pools"
    },
    {
      "name": "productionPools",
      "title": "# Production Pools"
    }
  ],
  "tip": "Use Host Pool deployed to Validation Environment to ensure deployment resilience and business functionality continuation"
}
---
