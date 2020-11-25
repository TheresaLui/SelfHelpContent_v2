<properties
    pageTitle="Accelerated Networking Disengaged"
    description="Accelerated Networking needs Stop and Start to re-engage"
    authors="SteveEsp"
    ms.author="SteveEsp"
    articleId="a06456ed-afb7-4d16-86fd-0054e25268ed_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, USSec, USNat"
	ownershipId="CloudNet_Datapath"
/>
# Accelerated Networking needs Stop and Start to re-engage 
---
{
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "a06456ed-afb7-4d16-86fd-0054e25268ed",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://vmainsight.kusto.windows.net').database('vmadbexp').AzAdvFn_DisengagedAccelNet_Public",
    "dataSource": "Kusto",
    "refreshInterval": "6:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Compute/virtualMachines",
  "recommendationFriendlyName": "AccelNetDisengaged",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "gftops@microsoft.com",
    "icm": {
      "routingId": "MDM://Cloudnet/AccelNet",
      "service": "Cloudnet",
      "team": "AccelNet"
    },
    "serviceTreeId": "1ff361e9-fa69-4549-8b0f-65edfe5a8709"
  },
  "ingestionClientIdentities": [],
  "version": 1.1,
  "learnMoreLink": "https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli#enable-accelerated-networking-on-existing-vms",
  "description": "Accelerated Networking may require stopping and starting the VM",
  "longDescription": "We have detected that Accelerated Networking is not engaged on a VM resources in your existing deployment even though the feature has been requested. In rare cases like this, it may be necessary to stop and start your VM, at your convenience, to re-engage AccelNet.",
  "potentialBenefits": "Improves performance throughput while reducing latency and jitter",
  "actions": [
    {
      "actionId": "4dca9be6-d668-4fc5-83aa-421a61c65f4e",
      "description": "Accelerated Networking needs Stop and Start to re-engage and improve network performance.",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "f1670b1d-cf96-4bda-a0e0-88129bfee3ad",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel":"Enable Accelerated Networking to improve network performance and latency",
  "additionalColumns": [],  "testData":"511d4d6c-766e-428e-96c6-1fcda5c34b0e,/subscriptions/511d4d6c-766e-428e-96c6-1fcda5c34b0e/resourceGroups/AzurePerformance/providers/Microsoft.Compute/virtualMachines/azperftest",
 "tip": "Accelerated Networking needs VM Stop then Start to improve network performance and latency."
}
---
