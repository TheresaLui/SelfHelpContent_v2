<properties
    pageTitle="Improve user experience and connectivity by deploying VMs closer to user's location."
    description="Improve user experience and connectivity by deploying VMs closer to user's location."
    authors="marius"
    ms.author="rdinfra"
    articleId="d89829c9-dadf-4ddc-87d6-fd746debd5d3_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, ussec, usnat"
    ownershipId="Windows_Virtual_Desktop"
/>
# Enable Validation Environment
---
{
  "recommendationOfferingId": "1132b618-fefe-40a0-9256-e685ff575ac7",
  "recommendationOfferingName": "Windows Virtual Desktop",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "d89829c9-dadf-4ddc-87d6-fd746debd5d3",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://rdsprodus2.westus2.kusto.windows.net').database('WVD').HostRegionShouldAlignWithGatewayRegion",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DesktopVirtualization/hostpools",
  "recommendationFriendlyName": "RegionProximityHostPools",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "rdinfra@microsoft.com",
    "icm": {
      "routingId": "mdm://adspartner/VirtualDesktop",
      "service": "Windows Virtual Desktop",
      "team": "Windows Virtual Desktop"
    },
    "serviceTreeId": "362c0db7-c08b-4471-93ef-c90effc930dd"
  },
  "ingestionClientIdentities": [],
  "version": 2.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/virtual-desktop/connection-latency",
  "description": "Improve user experience and connectivity by deploying VMs closer to user’s location.",
  "longDescription": "We have determined that your VMs are located in a region different or far from where your users are connecting from, using Windows Virtual Desktop (WVD). This may lead to prolonged connection response times and will impact overall user experience on WVD. When creating VMs for your host pools, you should attempt to use a region closer to the user. Having close proximity ensures continuing satisfaction with the WVD service and a better overall quality of experience.",
  "potentialBenefits": "Improves satisfaction with network round-trip time of the WVD service deployments.",
  "actions": [
    {
      "actionId": "c19a5909-324a-4922-a128-d8b14fc3b3c2",
      "description": "Deploy VMs in a Host to different region",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_WVD",
      "bladeName": "HostpoolOverviewBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "66b4371d-c4ef-475a-80b6-9cc212b2c008",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_WVD",
      "bladeName": "HostpoolOverviewBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Deploy VMs to different region",
  "additionalColumns": [
    {
      "name": "hostPoolRegion",
      "title": "Host Pool Region"
    },
    {
      "name": "gatewayRegion",
      "title": "Gateway Region"
    }
  ],
  "tip": "Use VMs from a region where users are located."
}
---
