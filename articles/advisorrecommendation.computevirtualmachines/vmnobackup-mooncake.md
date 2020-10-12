<properties
    pageTitle="Enable virtual machine backup to protect your data from corruption and accidental deletion"
    description="Enable virtual machine backup to protect your data from corruption and accidental deletion"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="af0be9f8-e590-48d0-9e19-380d8819b8dc_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
	ownershipId="StorageMediaEdge_Backup"
/>
# Enable virtual machine backup to protect your data from corruption and accidental deletion
---
{
  "recommendationOfferingId": "66abd0ce-a454-409f-9d69-b0c951a6b208",
  "recommendationOfferingName": "Backup",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "af0be9f8-e590-48d0-9e19-380d8819b8dc",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "azureadvisor.armvmnobackupv2_mooncake",
    "dataSource": "Cosmos",
    "refreshInterval": "01:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Compute/virtualMachines",
  "recommendationFriendlyName": "VmNoBackup",
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
  "version": 3.0,
  "learnMoreLink": "https://aka.ms/aa_vmbackup_learnmore_cn",
  "description": "Enable virtual machine backup to protect your data from corruption and accidental deletion",
  "longDescription": "Configure virtual machine backup to protect your mission critical data against accidental deletion or corruption.",
  "potentialBenefits": "Improved data resilience and performance",
  "actions": [
    {
      "actionId": "9cf732f3-065a-4549-be73-ae89785c0d77",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_RecoveryServices",
      "bladeName": "EnableBackupCommonBlade",
      "description": "Enable virtual machine backup",
      "metadata": {
        "backupManagementType": "AzureIaasVM",
        "properties": {
          "vmLocation": "{location}"
        },
        "resourceId": "{resourceId}",
        "workLoadType": "VM"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "669798c8-09f8-48bf-90ec-f11d35f9356d",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Enable Virtual Machine Backup",
  "additionalColumns": [],
  "legacyDataLoader": {
    "className": "Microsoft.Azure.Advisor.Common.DataLoaders.VmNoBackupResourceDataParser",
    "assemblyName": "Microsoft.Azure.Advisor.Common"
  },
  "tip": "You can enable virtual machine backup to protect your data from corruption or accidental deletion."
}
---
