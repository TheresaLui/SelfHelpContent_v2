<properties
    pageTitle="Convert Managed Disks from Standard HDD to Premium SSD"
    description="Convert Managed Disks from Standard HDD to Premium SSD"
    authors="xdataanalytics"
    ms.author="yinfan"
    articleId="e4fc6ecb-b3e8-4494-800f-547da6a57f28_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
	ownershipId="StorageMediaEdge_XStore"
/>
# Convert Standard HDD to Premium SSD for Performance
---
{
  "recommendationOfferingId": "c6b94711-f1f5-4e7e-9c89-c17ed4190969",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "00c14add-2aef-4bb4-a3bd-5759096d4417",
  "dataSourceMetadata": {
    "streamNamespace": "AzureStorage.Data.StorageAdvisorMDHDDtoPremiumForPerformanceMooncake",
    "dataSource": "Cosmos",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Compute/disks",
  "recommendationFriendlyName": "MDHDDtoPremiumForPerformance",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "yinfan@microsoft.com",
    "icm": {
      "routingId": "mdm://XStore/DataAnalytics",
      "service": "Xstore",
      "team": "Xstore/ Data Analytics"
    },
    "serviceTreeId": "734379f9-2d2c-48d4-a52a-5c509f699de4"
  },
  "version": 1.2,
  "learnMoreLink": "https://docs.microsoft.com/azure/virtual-machines/windows/disks-types#premium-ssd",
  "description": "Convert Managed Disks from Standard HDD to Premium SSD for performance",
  "longDescription": "We have noticed your Standard HDD disk is approaching performance targets. Azure premium SSDs deliver high-performance and low-latency disk support for virtual machines with IO-intensive workloads. Give your disk performance a boost by upgrading your Standard HDD disk to Premium SSD disk. Upgrading requires a VM reboot, which will take three to five minutes.",
  "potentialBenefits": "Give your disk performance a boost using Premium SSD disks.",
  "actions": [
   {
      "actionId": "27e5f4f3-2b65-4b94-8268-a15a49b0fbce",
      "description": "Convert Standard HDD to Premium SSD for better performance",
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
  "displayLabel": "Convert Standard HDD to Premium SSD for better performance",
  "testData": "65490f91-f2c2-4514-80ba-4ec1de89aeda,/subscriptions/65490f91-f2c2-4514-80ba-4ec1de89aeda/resourceGroups/XStoreDataAnalytics/providers/Microsoft.Storage/",
  "tip": "Upgrade your Standard HDD disks to Premium SSD disks by following our instructions for the Azure portal, PowerShell, or CLI."
}
---
