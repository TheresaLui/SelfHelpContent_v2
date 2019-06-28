<properties
    pageTitle="Use availability sets for improved fault tolerance"
    description="Use availability sets for improved fault tolerance"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="02c15f98-aedb-481b-884b-af5847b2bf3d_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
/>
# Use availability sets for improved fault tolerance
---
{
  "recommendationOfferingId": "07649cbd-2ee4-4992-898b-f5f16bad1b36",
  "recommendationOfferingName": "Virtual Machines",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "02c15f98-aedb-481b-884b-af5847b2bf3d",
  "dataSourceMetadata": {
    "schemaVersion": 1.0,
    "streamNamespace": "azureadvisor.vmsnotinavailabilitysets_mooncake",
    "dataSource": "Cosmos",
    "refreshInterval": "01:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Compute/virtualMachines",
  "recommendationFriendlyName": "SIVM",
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
  "version": 1.0,
  "learnMoreLink": "http://aka.ms/aa_sivmrec_learnmore_cn",
  "description": "Use availability sets for improved fault tolerance",
  "longDescription": "Group two or more virtual machines in an availability set to ensure at least one virtual machine is available during an outage.",
  "potentialBenefits": "Ensure business continuity through virtual machine resilience",
  "actions": [],
  "resourceMetadata": {
    "action": {
      "actionId": "91395c05-d944-49b4-92cb-764e20d42a04",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_Compute",
      "bladeName": "VirtualMachineBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Use availability sets",
  "additionalColumns": [],
  "legacyDataLoader": {
    "className": "Microsoft.Azure.Advisor.Common.DataLoaders.VmNotInAvailabilitySetDataParser",
    "assemblyName": "Microsoft.Azure.Advisor.Common"
  },
  "legacyRecommender": {
    "className": "Microsoft.Azure.Advisor.Common.Recommenders.VmNotInAvailabilitySetRecommender",
    "assemblyName": "Microsoft.Azure.Advisor.Common"
  }
}
---

