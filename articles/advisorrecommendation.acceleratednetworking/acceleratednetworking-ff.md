<properties
    pageTitle="Enable Accelerated Networking to improve network performance and latency"
    description="Enable Accelerated Networking to improve network performance and latency"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="9ce840f8-35b2-441d-bf3f-33084c3c4cc7_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
/>
# Enable Accelerated Networking to improve network performance and latency
---
{
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "9ce840f8-35b2-441d-bf3f-33084c3c4cc7",
  "dataSourceMetadata": {
    "streamNamespace": "cluster ('https://aznwff.kusto.usgovcloudapi.net').database('aznwcosmos').AzureAdvisorForANcapableVMs_FF",
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
      "actionId": "ec50b695-9d2d-4864-a5a6-45f911a64b3d",
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
      "actionId": "64a8857f-bfbd-4e0a-a67f-2da19c9ff420",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": " Enable Accelerated Networking to improve network performance and latency",
"tip": " Enable Accelerated Networking to improve network performance and latency."
}
---
