<properties
    pageTitle="Enable Accelerated Networking to improve network performance and latency"
    description="Enable Accelerated Networking to improve network performance and latency"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="3a3c1a2a-8597-4d3a-981a-0a24a0ee9de4_Usnat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Usnat"
    ownershipId="CloudNet_Datapath"
/>
# Enable Accelerated Networking to improve network performance and latency
---
{
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "3a3c1a2a-8597-4d3a-981a-0a24a0ee9de4",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://aznwsdn.usnatwest.kusto.core.eaglex.ic.gov').database('aznwmds').AzureAdvisorForANcapableVMs_USNat",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Compute/VirtualMachines",
  "recommendationFriendlyName": "AccelNetConfiguration",
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
  "version": 1.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/virtual-network/create-vm-accelerated-networking-cli#enable-accelerated-networking-on-existing-vms",
  "description": "Enable Accelerated Networking to improve network performance and latency",
  "longDescription":  "We have detected that Accelerated Networking is not enabled on VM resources in your existing deployment that may be capable of supporting this feature. If your VM OS image supports Accelerated Networking as detailed in the documentation, make sure to enable this free feature on these VMs to maximize the performance and latency of your networking workloads in cloud ",
  "potentialBenefits": "Improves performance throughput while reducing latency and jitter",
  "actions": [
    {
      "actionId": "cdd3139d-9dd0-48aa-82f8-9264f23707c5",
      "description": " Enable Accelerated Networking to improve network performance and latency ",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}",
	"menuid": "networking"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "bddfb8e9-6398-4e5f-9d53-434bc7351339",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel":"Enable Accelerated Networking to improve network performance and latency",
  "additionalColumns": [],
  "testData":"6c59adc2-2c7f-4f6f-a88e-6ef09e151cf6,/subscriptions/6c59adc2-2c7f-4f6f-a88e-6ef09e151cf6/resourceGroups/LX_SDN_Demo_Environment/providers/Microsoft.Compute/virtualMachines/ClientVM",
 "tip": "Enable Accelerated Networking to improve network performance and latency."
}
---
