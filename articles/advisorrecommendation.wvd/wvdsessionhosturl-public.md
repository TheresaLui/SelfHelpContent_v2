<properties
    pageTitle="Unblock proper URLs to ensure successful functionality of the VMs"
    description="Unblock proper URLs to ensure successful functionality of the VMs"
    authors="t-jajo"
    ms.author="rdinfra"
    articleId="53e0a3cb-3569-474a-8d7b-7fd06a8ec227_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, ussec, usnat"
    ownershipId="Windows_Virtual_Desktop"
/>
# Unblock required URLs
---
{
  "recommendationOfferingId": "1132b618-fefe-40a0-9256-e685ff575ac7",
  "recommendationOfferingName": "Windows Virtual Desktop",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "53e0a3cb-3569-474a-8d7b-7fd06a8ec227",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://rdsprodus2.westus2.kusto.windows.net').database('WVD').SessionHostNeedsAssistanceUrl",
    "dataSource": "Kusto",
    "refreshInterval": "0.01:00:00"
  },
  "recommendationCategory": "Reliability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.Compute/virtualMachines",
  "recommendationFriendlyName": "SessionHostNeedsAssistanceForUrlCheck",
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
  "version": 1.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/virtual-desktop/safe-url-list",
  "description": "Approval of necessary URL(s) missing",
  "longDescription": "In order for a session host to deploy and attach to WVD properly, you need to add a set of URLs to allowed list in case your virtual machine runs in restricted environment. After visiting \"Learn More\" link, you will be able to see the minimum list of URLs you need to unblock to have a successful deployment and functional session host. For specific URL(s) missing from allowed list, you may also search Application event log for event 3702.",
  "potentialBenefits": "Ensure successful deployment and session host functionality when using Windows Virtual Desktop service",
  "actions": [
    {
      "actionId": "5b82a65b-9006-4105-9fba-30571e5273d1",
      "description": "Unblock all URLs from the Safe URL list",
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
      "actionId": "46e242ab-0ccc-46fc-894d-dca0c6f98242",
      "actionType": "Blade",
      "extensionName": "Microsoft_Azure_WVD",
      "bladeName": "HostpoolOverviewBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Unblock all URLs from the Safe URL list",
  "additionalColumns": [],
  "tip": "Unblock all URLs from the Safe URL list to ensure a successful deployment of your VMs."
}
---
