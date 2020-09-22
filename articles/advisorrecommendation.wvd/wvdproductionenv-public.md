<properties
    pageTitle="Ensure production (non-validation) environment to benefit from stable functionality"
    description="Ensure production (non-validation) environment to benefit from stable functionality"
    authors="marius"
    ms.author="rdinfra"
    articleId="87269ca9-dda6-448e-97ac-c5888b2a2d61_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, ussec, usnat"
    ownershipId="Windows_Virtual_Desktop"
/>
# Enable Production Environment
---
{
  "recommendationOfferingId": "1132b618-fefe-40a0-9256-e685ff575ac7",
  "recommendationOfferingName": "Windows Virtual Desktop",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "87269ca9-dda6-448e-97ac-c5888b2a2d61",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://rdsprodus2.westus2.kusto.windows.net').database('WVD').SubscriptionNeedsProductionEnv",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "OperationalExcellence",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DesktopVirtualization/hostpools",
  "recommendationFriendlyName": "ProductionEnvHostPools",
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
  "learnMoreLink": "https://docs.microsoft.com/azure/virtual-desktop/create-host-pools-powershell",
  "description": "Not enough production environments enabled",
  "longDescription": "We have determined that too many of your host pools have Validation Environment enabled. In order for Validation Environments to best serve their purpose, you should have at least one, but never more than half of your host pools in Validation Environment. By having a healthy balance between your host pools with Validation Environment enabled and those with it disabled, you will best be able to utilize the benefits of the multistage deployments that Windows Virtual Desktop offers with certain updates. To fix this issue, open your host pool's properties and select \"No\" next to the \"Validation Environment\" setting.",
  "potentialBenefits": "Ensure functional stability and business continuity using Windows Virtual Desktop service",
  "actions": [
    {
      "actionId": "d106c31c-e4da-4418-aef9-33878467f11f",
      "description": "Deploy Host Pool to production (non-validation) environment",
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
      "actionId": "e27bc6a5-eabe-4165-9b1f-538048f7a5a3",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_WVD",
      "bladeName": "WvdManagerMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Deploy Host Pool to production (non-validation) environment",
  "additionalColumns": [],
  "tip": "Use Host Pool deployed to production (non-validation) environment to ensure business functionality continuation with increased stability"
}
---
