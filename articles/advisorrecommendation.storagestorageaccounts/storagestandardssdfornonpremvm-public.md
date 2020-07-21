<properties
    pageTitle="Use Standard SSD for performance on VMs that do not support Premium Disks"
    description="Use Standard SSD for performance on VMs that do not support Premium Disks"
    authors="lisson"
    ms.author="xdataanalytics"
    articleId="2df6d034-c368-405b-b909-2b5811055dba_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="StorageMediaEdge_XStore"
/>
# Use Standard SSD for performance on VMs that do not support Premium Disks
---
{
  "recommendationOfferingId": "6afdf2da-5218-4775-a020-b2aad5f6e4a6",
  "recommendationOfferingName": "Storage",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "8433e84a-8f5c-4b6c-9052-9b98757348ea",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://xstore.kusto.windows.net').database('xstore').StorageAdvisorStandardSSDForNonPremVMPublic",
    "dataSource": "Kusto",
    "refreshInterval": "1.00:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Storage/storageAccounts",
  "recommendationFriendlyName": "StandardSSDForNonPremVM",
  "recommendationMetadataState": "Enabled",
  "owner": {
    "email": "lisson@microsoft.com",
    "icm": {
      "routingId": "mdm://XStore/DataAnalytics",
      "service": "Xstore",
      "team": "Xstore/ Data Analytics"
    },
    "serviceTreeId": "734379f9-2d2c-48d4-a52a-5c509f699de4"
  },
  "version": 2,
  "learnMoreLink": "https://docs.microsoft.com/azure/virtual-machines/windows/disks-types#standard-ssd",
  "description": "Upgrade to Standard SSD Disks for consistent and improved performance",
  "longDescription": "Because you are running IaaS virtual machine workloads on Standard HDD managed disks, we wanted to let you know that a Standard SSD disk option is now available for all Azure VM types. Standard SSD disks are a cost-effective storage option optimized for enterprise workloads that need consistent performance. Upgrade your disk configuration today for improved latency, reliability, and availability. Upgrading requires a VM reboot, which will take three to five minutes.",
  "potentialBenefits": "Improve disk latency, reliability, and availability using Standard SSD disks.",
  "actions": [
   {
      "actionId": "1ff870e9-1f31-4c81-9a71-cb6f48dd0c2c",
      "description": "Use Standard SSD for performance on VMs that do not support Premium Disks",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/virtual-machines/windows/convert-disk-storage"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "71329c29-f4d1-436a-8969-49442a39d358",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Storage",
      "bladeName": "StorageAccountBlade",
      "metadata": {
        "id": "{resourceId}"
      },
      "documentLink": "https://docs.microsoft.com/azure/virtual-machines/windows/convert-disk-storage"
    }
  },
  "displayLabel": "Upgrade to Standard SSD Disks for consistent and improved performance",
  "testData": "65490f91-f2c2-4514-80ba-4ec1de89aeda,/subscriptions/65490f91-f2c2-4514-80ba-4ec1de89aeda/resourceGroups/XStoreDataAnalytics/providers/Microsoft.Compute/",
  "tip": "Upgrade to Standard SSD Disks for consistent and improved performance by following our instructions for the Azure portal, PowerShell, or CLI."
}
---
