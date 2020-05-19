<properties
    pageTitle="Use Managed disks to prevent disk I/O throttling"
    description="Use Managed disks to prevent disk I/O throttling"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="36c3633b-daac-4e01-af95-11b8c2f4fe20_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
	ownershipId="StorageMediaEdge_XStore"
/>
# Use Managed disks to prevent    disk I/O throttling
---
{
  "recommendationOfferingId": "c6b94711-f1f5-4e7e-9c89-c17ed4190969",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "36c3633b-daac-4e01-af95-11b8c2f4fe20",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "azureadvisor.manageddiskstorageaccount4_mooncake",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Compute/virtualMachines",
  "recommendationFriendlyName": "ManagedDisksStorageAccount",
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
  "description": "Use Managed disks to prevent disk I/O throttling",
  "longDescription": "Your virtual machine disks belong to a storage account that has reached its scalability target, and is susceptible to I/O throttling. To protect your virtual machine from performance degradation and to simplify storage management, use Managed Disks.",
  "potentialBenefits": "Improved data resilience and performance",
  "actions": [
    {
      "actionId": "81a42007-5d9c-4af3-b8ff-d10f3aadf25b",
      "description": "Migrate to Managed Disks",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Compute",
      "bladeName": "VirtualMachineMigrateToManagedDisksBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "a146fc44-bb83-48d6-b5ca-2d4746fa398f",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Compute",
      "bladeName": "VirtualMachineBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Use Managed Disks",
  "additionalColumns": [],
  "tip": "You can use Managed Disks to prevent disk throttling and improve virtual machine performance.",
  "learnMoreLink": "https://aka.ms/aa_avset_manageddisk_learnmore_cn"
}
---
