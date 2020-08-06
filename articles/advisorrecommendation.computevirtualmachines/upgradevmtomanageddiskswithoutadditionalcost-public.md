<properties
    pageTitle="Upgrade VM from Premium Unmanaged Disks to Managed Disks at no additional cost"
    description="Upgrade VM from Premium Unmanaged Disks to Managed Disks at no additional cost"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="57ecb3cd-f2b4-4cad-8b3a-232cca527a0b_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="StorageMediaEdge_XStore"
/>
# Upgrade VM from Premium Unmanaged Disks to Managed Disks at no additional cost
---
{
  "recommendationOfferingId": "c6b94711-f1f5-4e7e-9c89-c17ed4190969",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "57ecb3cd-f2b4-4cad-8b3a-232cca527a0b",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "azurestorage.data.storageadvisormigratetomdwithnoadditionalcostpublic",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Compute/virtualMachines",
  "recommendationFriendlyName": "UpgradeVMToManagedDisksWithoutAdditionalCost",
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
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/md_overview",
  "description": "Upgrade VM from Premium Unmanaged Disks to Managed Disks at no additional cost",
  "longDescription": "We have identified that your VM is using premium unmanaged disks that can be migrated to managed disks at no additional cost. Azure Managed Disks provides higher resiliency, simplified service management, higher scale target and more choices among several disk types. This upgrade can be done through the portal in less than 5 minutes.",
  "potentialBenefits": "Leverage higher resiliency and other benefits of Managed Disks",
  "actions": [
    {
      "actionId": "0a52c8b8-5200-443f-9e04-2d233162451b",
      "description": "Upgrade VM to Managed Disks at no additional cost",
      "actionType": "Document",
      "documentLink": "https://aka.ms/migrate_to_md"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "99d92b69-47ae-49e9-8062-b64325868e91",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Upgrade VM to Managed Disks at no additional cost",
  "additionalColumns": []
}
---
