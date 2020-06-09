<properties
    pageTitle="Use availability sets for improved fault tolerance"
    description="Use availability sets for improved fault tolerance"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="02c15f98-aedb-481b-884b-af5847b2bf3d_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="Compute_VirtualMachines"
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
    "streamNamespace": "azureadvisor.vmsnotinavailabilitysets",
    "dataSource": "Cosmos",
    "refreshInterval": "01:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Compute/virtualMachines",
  "recommendationFriendlyName": "SIVM",
  "recommendationMetadataState": "Disabled",
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
  "version": 2.0,
  "learnMoreLink": "https://aka.ms/aa_sivmrec_learnmore",
  "description": "Use availability sets for improved fault tolerance",
  "longDescription": "Group two or more virtual machines in an availability set to ensure at least one virtual machine is available during an outage.",
  "potentialBenefits": "Ensure business continuity through virtual machine resilience",
  "actions": [
    {
      "actionId": "7C9876C8-E6CB-4DC9-8865-39E4EA2CD384",
      "actionType": "Document",
      "description": "Move the virtual machine into an existing availability set",
      "documentLink": "https://aka.ms/aa_sivmrec_arm_action1"
    },
    {
      "actionId": "6BE7BED7-4847-48B1-890E-4987A4362CFE",
      "actionType": "Document",
      "description": "Move the virtual machine into a new availability set",
      "documentLink": "https://aka.ms/aa_sivmrec_arm_action2"
    }
  ],
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
  }
}
---
