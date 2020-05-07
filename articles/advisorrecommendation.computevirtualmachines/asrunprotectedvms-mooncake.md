<properties
    pageTitle="Enable virtual machine replication to protect your applications from regional outage"
    description="Enable virtual machine replication to protect your applications from regional outage"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="ed651749-cd37-4fd5-9897-01b416926745_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="Compute_SiteRecovery"
/>
# Enable virtual machine replication to protect your applications from regional outage
---
{
  "recommendationOfferingId": "59258b9f-d209-420b-bdd3-7331f87c929e",
  "recommendationOfferingName": "Site Recovery",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "ed651749-cd37-4fd5-9897-01b416926745",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "AzureAdvisor.ASRUnprotectedVMs_MoonCake",
    "dataSource": "Cosmos",
    "refreshInterval": "01:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Compute/virtualMachines",
  "recommendationFriendlyName": "ASRUnprotectedVMs",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "bcdrasrfte@microsoft.com",
    "icm": {
      "routingId": "MDM://MASR-Mooncake",
      "service": "Azure Site Recovery - China/Gallatin",
      "team": "Microsoft Azure Site Recovery Engineering"
    },
    "serviceTreeId": "5d0f2841-795b-49c6-9ab1-c2195fc9a4ea"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/azure-site-recovery-dr-azure-vms",
  "description": "Enable virtual machine replication to protect your applications from regional outage",
  "longDescription": "Virtual machines which do not have replication enabled to another region are not resilient to regional outages. Replicating the machines drastically reduce any adverse business impact during the time of an Azure region outage. We highly recommend enabling replication of all the business critical virtual machines from the below list so that in an event of an outage, you can quickly bring up your machines in remote Azure region.",
  "potentialBenefits": "Ensure business continuity in case of any Azure region outage",
  "actions": [
    {
      "actionId": "a8f85e23-e136-4e18-afb6-1e3ca5285db1",
      "description": "Enable virtual machine replication",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_RecoveryServices",
      "bladeName": "IaaSVmProtectionBlade2",
      "metadata": {
        "iaasVmArmId": "{resourceId}"
      }
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
  "displayLabel": "Enable virtual machine replication",
  "additionalColumns": []
}
---
