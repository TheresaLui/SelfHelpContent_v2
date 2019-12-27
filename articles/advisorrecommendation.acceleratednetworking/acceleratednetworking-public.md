<properties
    pageTitle="Enable Accelerated Networking to improve network performance and latency"
    description="Enable Accelerated Networking to improve network performance and latency"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="3a3c1a2a-8597-4d3a-981a-0a24a0ee9de4_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public"
/>
# Enable Accelerated Networking to improve network performance and latency 
---
{
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "3a3c1a2a-8597-4d3a-981a-0a24a0ee9de4",
  "dataSourceMetadata": {
    "streamNamespace": "cluster ('https://vmainsight.kusto.windows.net').database('vmaexpdb').AzureAdvisorForANcapableVMs",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Compute/virtualMachines",
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
  "longDescription": "We have detected that Accelerated Networking was disabled on your VM resources of existing deployment.Your VM resources are capable of supporting Accelerated Networking.Make sure to enable Accelerated Networking for existing VM to mitigate the impact on performance and latency of end-to-end network connectivity with latency senstive workloads in cloud",
  "potentialBenefits": "Improves performance throughput while reducing latency and jitter",
  "actions": [
    {
      "actionId": "e0efec31-2bed-4168-a8d2-58ca3cd5a1ff",
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
      "actionId": "03aae5ac-6787-42d0-ba66-8d51380035eb",
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
  "testData":"014e7430-fd92-4579-9119-e861d926508a,/subscriptions/014e7430-fd92-4579-9119-e861d926508a/resourceGroups/laxmanrb-BLAPrdApp27-rg/providers/Microsoft.Compute/virtualMachines/cx3vm-ds5v2-1",
 "tip": "Enable Accelerated Networking to improve network performance and latency."
}
---
