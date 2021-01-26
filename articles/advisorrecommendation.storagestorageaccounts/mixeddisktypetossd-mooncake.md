<properties
    pageTitle="Use SSD Disks for your production workloads"
    description="Use SSD Disks for your production workloads"
    authors="xdataanalytics"
    ms.author="yinfan"
    articleId="03f77f51-31a0-410c-ac76-165bf21d4d3f_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
cloudEnvironments="Mooncake"
ownershipId="StorageMediaEdge_XStore"
/>
# Use SSD Disks for your production workloads
---
{
  "recommendationOfferingId": "c3c3299d-ee34-4610-844d-3782d691a7fe",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "6747b02b-b6ac-4c2e-aeca-c2aa0438f58d",
  "dataSourceMetadata": {
    "streamNamespace": "AzureStorage.Data.StorageAdvisorMixedDiskTypesToSSD_Mooncake",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Compute/virtualMachines",
  "recommendationFriendlyName": "MixedDiskTypeToSSDPublic",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "xdataanalytics@microsoft.com",
    "icm": {
      "routingId": "mdm://XStore/DataAnalytics",
      "service": "Xstore",
      "team": "Xstore/ Data Analytics"
    },
    "serviceTreeId": "734379f9-2d2c-48d4-a52a-5c509f699de4"
  },
  "version": 1.1,
  "learnMoreLink": "https://docs.microsoft.com/azure/virtual-machines/windows/disks-types#disk-comparison",
  "description": "Use SSD Disks for your production workloads",
  "longDescription": "We noticed that you are using SSD disks while also using Standard HDD disks on the same VM. Standard HDD managed disks are generally recommended for dev-test and backup; we recommend you use Premium SSDs or Standard SSDs for production. Premium SSDs deliver high-performance and low-latency disk support for virtual machines with IO-intensive workloads. Standard SSDs provide consistent and lower latency. Upgrade your disk configuration today for improved latency, reliability, and availability. Upgrading requires a VM reboot, which will take three to five minutes.",
  "potentialBenefits": "Improve latency, reliability, and availability",
  "actions": [
   {
      "actionId": "140099f4-b336-4685-8a58-f327e140ff14",
      "description": "Use SSD Disks for your production workloads",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/virtual-machines/windows/convert-disk-storage"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "3599953d-b060-4884-8c7f-aa488d61253b",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Storage",
      "bladeName": "StorageAccountBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Use SSD Disks for your production workloads",
  "tip": ""
}
---
