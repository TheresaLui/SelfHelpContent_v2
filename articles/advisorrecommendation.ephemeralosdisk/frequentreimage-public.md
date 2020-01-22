<properties
    pageTitle="Use Ephemeral OS Disk VMs for more performance"
    description="For frequent reimage operations, prefer IaaS VMs with Ephemeral OS Disk"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="9768be7c-ad70-4870-af7b-e814000a5743_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
/>
# Create an Ephemeral OS Disk recommendation
---
{
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "9768be7c-ad70-4870-af7b-e814000a5743",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://azcrp.kusto.windows.net').database('crp_allprod').EphemeralCreateVmStats",
    "dataSource": "Kusto",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Compute/availabilitySets",
  "recommendationFriendlyName": "EphemeralOsDisk",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "ramsaic@microsoft.com",
    "icm": {
      "routingId": "MDM://Azure/Billing",
      "service": "Azure",
      "team": "Azure"
    },
    "serviceTreeId": "12345678-9012-3456-7890-123456789012"
  },
  "ingestionClientIdentities": [],
  "version": 1.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/vpn-gateway/vpn-gateway-about-vpn-gateway-settings#gwsku",
  "description": "Use Ephemeral OS Disk VMs for more performance",
  "longDescription": "For frequent reimage operations, prefer IaaS VMs with Ephemeral OS Disk.",
  "potentialBenefits": "Get notified when Azure finds it can optimize your VMs performance",
  "actions": [
    {
      "actionId": "f8db3c62-8ed7-48ea-b313-83c7224a5c47",
      "description": "Create an Azure service health alert",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Monitoring",
      "bladeName": "CreateVNextAlertRuleBlade",
      "metadata": {
        "ruleInputs": {
          "signals": [
            {
              "subscription": "{subscriptionId}",
              "signalType": "ServiceHealth",
              "targetService": [],
              "region": [],
              "type": []
            }
          ]
        }
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "da0fc147-5d91-4469-800a-3b621d41a8b2",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Create an Azure service health alert",
  "additionalColumns": [],
  "supportedSDKLanguages":[
      ".Net",
      "Java"
  ]
  "testData": "658c8950-e79d-4704-a903-1df66ba90258,/subscriptions/658c8950-e79d-4704-a903-1df66ba90258",
  "tip": "You can create a service health alert to get notified when an Azure service issue affects you."
}
---
