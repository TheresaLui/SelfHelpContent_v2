<properties
    pageTitle="Convert Unmanaged Disks from Standard HDD to Premium SSD"
    description="Convert Unmanaged Disks from Standard HDD to Premium SSD for Preformance"
    authors="yuriic"
    ms.author="xdataanalytics"
    articleId="e4fc6ecb-b3e8-4494-800f-547da6a57f28_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
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
    "streamNamespace": "cluster('https://xstore.kusto.windows.net').database('xstore').StorageAdvisorUMDHDDtoPremiumForPerformancePublic",
    "dataSource": "Kusto",
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
  "version": 1,
  "learnMoreLink": "https://docs.microsoft.com/azure/virtual-machines/windows/disks-types#premium-ssd",
  "description": "Convert Unmanaged Disks from Standard HDD to Premium SSD for performance",
  "longDescription": "We have noticed your Unmanaged HDD Disk is approaching performance targets. Azure premium SSDs deliver high-performance and low-latency disk support for virtual machines with IO-intensive workloads. Give your disk performance a boost by upgrading your Standard HDD disk to Premium SSD disk. Upgrading requires a VM reboot, which will take three to five minutes.",
  "potentialBenefits": "Give your disk performance a boost using Premium SSD disks.",
  "actions": [
   {
      "actionId": "27e5f4f3-2b65-4b94-8268-a15a49b0fbce",
      "description": "Convert Unmanaged Disks from Standard HDD to Premium SSD for better performance",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/virtual-machines/windows/convert-disk-storage"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "98be5cee-a61c-47bc-b063-0a00eac1b5be",
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
  "testData": "65490f91-f2c2-4514-80ba-4ec1de89aeda,/subscriptions/65490f91-f2c2-4514-80ba-4ec1de89aeda/resourceGroups/XStoreDataAnalytics/providers/Microsoft.Storage/",
  "tip": "Upgrade your Unmanaged HDD disks to Premium SSD disks by following our instructions for the Azure portal, PowerShell, or CLI."
}
---
