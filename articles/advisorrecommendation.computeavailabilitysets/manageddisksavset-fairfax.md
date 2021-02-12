<properties
    pageTitle="Use Managed Disks to improve data reliability"
    description="Use Managed Disks to improve data reliability"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="02cfb5ef-a0c1-4633-9854-031fbda09946_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="StorageMediaEdge_XStore"
/>
# Use Managed Disks to improve data reliability 
---
{
  "recommendationOfferingId": "c6b94711-f1f5-4e7e-9c89-c17ed4190969",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "02cfb5ef-a0c1-4633-9854-031fbda09946",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "azureadvisor.manageddisksinavailabilitysetv12_fairfax",
    "dataSource": "Cosmos",
    "refreshInterval": "01:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Compute/availabilitySets",
  "recommendationFriendlyName": "ManagedDisksAvSet",
  "recommendationMetadataState": "Disabled",
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
  "learnMoreLink": "https://aka.ms/aa_avset_manageddisk_learnmore",
  "description": "Use Managed Disks to improve data reliability",
  "longDescription": "Virtual machines in an Availability Set with disks that share either storage accounts or storage scale units are not resilient to single storage scale unit failures during outages. Migrate to Azure Managed Disks to ensure that the disks of different VMs in the Availability Set are sufficiently isolated to avoid a single point of failure.",
  "potentialBenefits": "Ensure business continuity through data resilience",
  "actions": [
    {
      "actionId": "184ffcd3-4dbb-41f3-9b4a-b4c47ee9312d",
      "description": "Migrate your availability set to use Managed Disks",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Compute",
      "bladeName": "AvailabilitySetMigrateBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "7dde0f77-6ac4-4b2b-83ad-74c183dfc7d7",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Use Managed Disks",
  "additionalColumns": [],
  "tip": "You can use Managed Disks to ensure data resilience."
}
---
