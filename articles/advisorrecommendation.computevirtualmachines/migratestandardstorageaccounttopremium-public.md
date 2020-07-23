<properties
    pageTitle="Upgrade the standard disks attached to your premium-capable VM to premium disks"
    description="Upgrade the standard disks attached to your premium-capable VM to premium disks"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="58d6648d-32e8-4346-827c-4f288dd8ca24_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="StorageMediaEdge_XStore"
/>
# Upgrade the standard disks attached to your premium-capable VM to premium disks
---
{
  "recommendationOfferingId": "c6b94711-f1f5-4e7e-9c89-c17ed4190969",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "58d6648d-32e8-4346-827c-4f288dd8ca24",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "azurestorage.data.storageadvisorstandardtopremiummigrationpublic",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Compute/virtualMachines",
  "recommendationFriendlyName": "MigrateStandardStorageAccountToPremium",
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
  "learnMoreLink": "https://aka.ms/aa_storagestandardtopremium_learnmore",
  "description": "Upgrade the standard disks attached to your premium-capable VM to premium disks",
  "longDescription": "We have identified that you are using standard disks with your premium-capable Virtual Machines and we recommend you consider upgrading the standard disks to premium disks. For any Single Instance Virtual Machine using premium storage for all Operating System Disks and Data Disks, we guarantee you will have Virtual Machine Connectivity of at least 99.9%. When making your upgrade decision, there are two factors to consider. The first is that upgrading requires a VM reboot and this process takes 3-5 minutes to complete. The second is if the VMs in the list are mission-critical production VMs, evaluate the improved availability against the cost of premium disks.",
  "potentialBenefits": "Improved availability with single VM SLA available only when all disks are premium",
  "actions": [
    {
      "actionId": "2d95a799-5e18-4507-874c-0bb488626ebc",
      "description": "Migrate your managed disks from Standard to Premium",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aa_storagestandardtopremium_action1"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "6a634d3b-4b12-4546-b895-b70a141a175e",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Migrate Standard disks to Premium disks",
  "additionalColumns": []
}
---
