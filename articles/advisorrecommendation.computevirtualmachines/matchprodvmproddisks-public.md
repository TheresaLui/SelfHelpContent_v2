<properties
    pageTitle="Match production Virtual Machines with Production Disk for consistent performance and better latency"
    description="Match Production Virtual Machine with Production Disks"
    authors="xdataanalytics"
    ms.author="xdataanalytics"
    articleId="9b0d1cf7-8a3a-4c8b-8f9f-1c3e70e399d6_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, USSec, USNat"
    ownershipId="StorageMediaEdge_XStore"
/>
# Enable virtual machine replication to protect your applications from regional outage
---
{
  "recommendationOfferingId": "c3c3299d-ee34-4610-844d-3782d691a7fe",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "9b0d1cf7-8a3a-4c8b-8f9f-1c3e70e399d6",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "AzureStorage.Data.MatchProdVMProdDiskPublicV1",
    "dataSource": "Cosmos",
    "refreshInterval": "01:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Compute/virtualMachines",
  "recommendationFriendlyName": "MatchProdVMProdDisks",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "xdataanalytics@microsoft.com",
    "icm": {
      "routingId": "mdm://XStore/DataAnalytics",
      "service": "Xstore",
      "team": "Xstore/ Data Analytics"
    },
    "serviceTreeId": "734379f9-2d2c-48d4-a52a-5c509f699de4"
  },
  "version": 1.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/virtual-machines/windows/disks-types#disk-comparison",
  "description": "Match production Virtual Machines with Production Disk for consistent performance and better latency",
  "longDescription": "Production virtual machines need production disks if you want to get the best performance. We see that you are running a production level virtual machine, however, you are using a low performing disk with standard HDD. Upgrading your disks that are attached to your production disks, either Standard SSD or Premium SSD, will benefit you with a more consistent experience and improvements in latency.",
  "potentialBenefits": "More consistent performance, better latency",
  "actions": [
    {
      "actionId": "3a7d78f7-276d-4771-b2e0-84f129a110cf",
      "description": "Match Production Virtual Machine with Production Disks",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/virtual-machines/windows/migrate-to-premium-storage-using-azure-site-recovery"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "e2377fed-d17f-499e-b722-fa59070ebad2",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Storage",
      "bladeName": "StorageAccountBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Match production Virtual Machines with Production Disk for consistent performance and better latency",
  "additionalColumns": [],
  "tip": "Match Production Virtual Machine with Production Disks.",
  "learnMoreLink": "https://docs.microsoft.com/azure/virtual-machines/windows/disks-types#disk-comparison",
  "testData": "95fd5dac-4367-43b4-bf59-39daf2603153,/subscriptions/95fd5dac-4367-43b4-bf59-39daf2603153/resourceGroups/prakashRG/providers/Microsoft.Compute/virtualMachines/manageddisksvm"
}
---
