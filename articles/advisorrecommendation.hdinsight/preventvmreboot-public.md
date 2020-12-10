<properties
    pageTitle="Prevent HDInsight cluster VMs from rebooting periodically"
    description="Prevent HDInsight cluster VMs from rebooting periodically"
    authors="xunwei"
    ms.author="xunwei"
    articleId="353bcb88-3747-4a7a-8b1c-374117db5668_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureData_HDInsight"
/>
# Prevent HDInsight cluster VMs from rebooting periodically
---
{
  "recommendationOfferingId": "e24dace6-5068-4c13-b6b7-88b7b6e8a577",
  "recommendationOfferingName": "HDInsight",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "353bcb88-3747-4a7a-8b1c-374117db5668",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://hdinsight.kusto.windows.net').database('HDInsight').AllClustersInLastHr",
    "dataSource": "Kusto",
    "refreshInterval": "01:00:00"
  },
  "recommendationCategory": "Reliability",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.HDInsight/clusters",
  "recommendationFriendlyName": "PreventVMReboot",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "hdicorepm@microsoft.com",
    "icm": {
      "routingId": "MDM://HDInsight PM Team",
      "service": "HDInsight",
      "team": "HDInsight PM Team"
    },
    "serviceTreeId": "2ee735d6-5f03-45c3-bf11-fc1dbb1aa135"
  },
  "ingestionClientIdentities": [],
  "version": 1.0,
  "description": "Starting from mid November 2020, you may have noticed HDInsight cluster VMs getting rebooted on a regular basis. This could be caused by:
1.	Clamav is enabled on your cluster. The new azsec-clamav package consumes large amount of memory which triggers node rebooting. 
2.	A CRON job is scheduled daily that monitors for changes to the list of certificate authorities (CAs) used by Azure services. When a new CA certificate is available, the script adds the certificate to the JDK trust store and schedules a reboot.
HDInsight is deploying fixes and applying patch for all running clusters for both issues. To apply the fix immediately and avoid unexpected VMs rebooting, you can run below script actions on all cluster nodes as a persistent script action. HDInsight will post another notice after the fix and patching complete.
https://hdiconfigactions.blob.core.windows.net/linuxospatchingrebootconfigv02/replace_cacert_script.sh
https://healingscriptssa.blob.core.windows.net/healingscripts/ChangeOOMPolicyAndApplyLatestConfigForClamav.sh",
  "actions": [
    {
      "actionId": "d9634cc2-681f-4abc-81a3-4b6adee00eaf",
      "description": "Download script replace_cacert_script",
      "actionType": "Document",
      "documentLink": "https://hdiconfigactions.blob.core.windows.net/linuxospatchingrebootconfigv02/replace_cacert_script.sh"
    },
    {
      "actionId": "b4ac5e85-c603-498d-bdd9-aaced482a414",
      "description": "Download script ChangeOOMPolicyAndApplyLatestConfigForClamav",
      "actionType": "Document",
      "documentLink": "https://healingscriptssa.blob.core.windows.net/healingscripts/ChangeOOMPolicyAndApplyLatestConfigForClamav.sh"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "9d1c1947-3085-468f-adc4-71381f8fb2ee",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Prevent HDInsight cluster VMs from rebooting periodically",
  "additionalColumns": [],
  "tip": "Prevent HDInsight cluster VMs from rebooting periodically",
  "testData": "c36fd9e7-e5b1-4d3e-bb85-2e538040258b,/subscriptions/c36fd9e7-e5b1-4d3e-bb85-2e538040258b/resourceGroups/sw-shc/providers/Microsoft.HDInsight/clusters/swrhctest"
}
---
