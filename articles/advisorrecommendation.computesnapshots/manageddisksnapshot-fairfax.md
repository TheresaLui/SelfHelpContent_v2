<properties
    pageTitle="Use Standard Storage to store Managed Disks snapshots"
    description="Use Standard Storage to store Managed Disks snapshots"
    authors="aadevteam"
    ms.author="yuriic"
    articleId="702b474d-698f-4029-9f9d-4782c626923e_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="StorageMediaEdge_XStore"
/>
# Use Standard Storage to store Managed Disks snapshots
---
{
  "recommendationOfferingId": "c6b94711-f1f5-4e7e-9c89-c17ed4190969",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "702b474d-698f-4029-9f9d-4782c626923e",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "AzureStorage.Data.StorageAdvisorManagedDiskSnapshotV1_Fairfax",
    "dataSource": "Cosmos",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Compute/snapshots",
  "recommendationFriendlyName": "ManagedDiskSnapshot",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "Sijia.Zhu@microsoft.com",
    "icm": {
      "routingId": "mdm://XStore/DataAnalytics",
      "service": "Xstore",
      "team": "Xstore/ Data Analytics"
    },
    "serviceTreeId": "734379f9-2d2c-48d4-a52a-5c509f699de4"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/aa_manageddisksnapshot_learnmore",
  "description": "Use Standard Storage to store Managed Disks snapshots",
  "longDescription": "To save 60% of cost, we recommend storing your snapshots in Standard Storage, regardless of the storage type of the parent disk. This is the default option for Managed Disks snapshots. Migrate your snapshot from Premium to Standard Storage. Refer to Managed Disks pricing details.",
  "potentialBenefits": "60% reduction in the snapshot cost for Managed Disks",
  "actions": [
    {
      "actionId": "53f6af69-a145-49e0-8288-cb3c74a07ebc",
      "description": "Migrate Managed Disk snapshot using PowerShell ",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aa_manageddisksnapshot_action1"
    },
    {
      "actionId": "eb88b823-af4e-46e0-b2c7-6a5d4a2b798f",
      "description": "Migrate Managed Disk snapshot using CLI",
      "actionType": "Document",
      "documentLink": "https://aka.ms/aa_manageddisksnapshot_action2"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "d9e03004-3e58-45cd-81e6-84c3e289883d",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Use Standard snapshots for Managed Disks",
  "additionalColumns": []
}
---
