<properties
    pageTitle="Update your outbound connectivity protocol to Service Tags for Azure Site Recovery"
    description="Update your outbound connectivity protocol to Service Tags for Azure Site Recovery"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="bcfeb92b-fe93-4cea-adc6-e747055518e9_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="Compute_SiteRecovery"
/>
# Update your outbound connectivity protocol to Service Tags for Azure Site Recovery
---
{
  "recommendationOfferingId": "59258b9f-d209-420b-bdd3-7331f87c929e",
  "recommendationOfferingName": "Site Recovery",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "bcfeb92b-fe93-4cea-adc6-e747055518e9",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "cluster('https://asrclus1.kusto.windows.net').database('ASRKustoDB').GetIPWhitelistedSubscriptionAndVmArmId",
    "dataSource": "Kusto",
    "refreshInterval": "06:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Compute/virtualMachines",
  "recommendationFriendlyName": "ASRUpdateOutboundConnectivityProtocolToServiceTags",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "bcdrasrfte@microsoft.com",
    "icm": {
      "routingId": "MDM://MASR-PROD",
      "service": "Azure Site Recovery",
      "team": "Microsoft Azure Site Recovery Engineering"
    },
    "serviceTreeId": "5d0f2841-795b-49c6-9ab1-c2195fc9a4ea"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/azure-site-recovery-using-service-tags",
  "description": "Update your outbound connectivity protocol to Service Tags for Azure Site Recovery",
  "longDescription": "Using IP Address based whitelisting has been identified as a vulnerable way to control outbound connectivity for firewalls. It is advised to use Service Tags as an alternative for controlling connectivity. We highly recommend the use of Service Tags, to allow connectivity to Azure Site Recovery services for the machines.",
  "potentialBenefits": "Ensures better security, stability and resiliency than hard coded IP Addresses",
  "actions": [
    {
      "actionId": "a8900d46-6b9a-4f2a-9fa3-0069da87f095",
      "description": "Switch outbound connectivity protocol to Service Tags for Azure Site Recovery services",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/site-recovery/azure-to-azure-about-networking#outbound-connectivity-using-service-tags"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "5a69f1fa-2b6d-4e96-b212-0c023f680872",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Update your outbound connectivity protocol to Service Tags for Azure Site Recovery",
  "additionalColumns": []
}
---
