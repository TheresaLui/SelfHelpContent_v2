<properties
    pageTitle="Convert Unmanaged Disks from Standard HDD to Premium SSD"
    description="Convert Unmanaged Disks from Standard HDD to Premium SSD for Preformance"
    authors="yinfan"
    ms.author="xdataanalytics"
    articleId="33557a7c-6dd6-4b46-9579-fc5273f07458_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="StorageMediaEdge_XStore"
/>
# Convert Standard HDD to Premium SSD for Performance
---
{
  "recommendationOfferingId": "c6b94711-f1f5-4e7e-9c89-c17ed4190969",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "33557a7c-6dd6-4b46-9579-fc5273f07458",
  "dataSourceMetadata": {
    "streamNamespace": "AzureStorage.Data.StorageAdvisorUMDHDDtoPremiumForPerformanceFairfax",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Storage/storageAccounts",
  "recommendationFriendlyName": "UMDHDDtoPremiumForPerformance",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "yuriic@microsoft.com",
    "icm": {
      "routingId": "mdm://XStore/DataAnalytics",
      "service": "Xstore",
      "team": "Xstore/ Data Analytics"
    },
    "serviceTreeId": "734379f9-2d2c-48d4-a52a-5c509f699de4"
  },
  "version": 1.1,
  "learnMoreLink": "https://docs.microsoft.com/azure/virtual-machines/windows/disks-types#premium-ssd",
  "description": "Convert Unmanaged Disks from Standard HDD to Premium SSD for performance",
  "longDescription": "We have noticed your Unmanaged HDD Disk is approaching performance targets. Azure premium SSDs deliver high-performance and low-latency disk support for virtual machines with IO-intensive workloads. Give your disk performance a boost by upgrading your Standard HDD disk to Premium SSD disk. Upgrading requires a VM reboot, which will take three to five minutes.",
  "potentialBenefits": "Give your disk performance a boost using Premium SSD disks.",
  "actions": [
   {
      "actionId": "9ee50012-09cf-4d87-b23b-a59dcf8d5ae3",
      "description": "Convert Unmanaged Disks from Standard HDD to Premium SSD for better performance",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/virtual-machines/windows/convert-disk-storage"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "7f7e9668-95df-4b04-b529-68b1734e866f",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Storage",
      "bladeName": "StorageAccountBlade",
      "metadata": {
        "id": "{resourceId}"
      },
      "documentLink": "https://docs.microsoft.com/azure/virtual-machines/windows/convert-disk-storage"
    }
  },
  "displayLabel": "Convert Unmanaged Disks from Standard HDD to Premium SSD for performance",
  "tip": "Upgrade your Unmanaged HDD disks to Premium SSD disks by following our instructions for the Azure portal, PowerShell, or CLI."
}
---
