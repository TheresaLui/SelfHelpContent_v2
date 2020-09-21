<properties
    pageTitle="Right-size or shutdown underutilized virtual machines"
    description="Right-size or shutdown underutilized virtual machines"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="d472fb24-d23c-480f-896f-b3095d5bd868_ussec"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="ussec"
	ownershipId="CloudFit_CostOptimization"
/>
# Right-size or shutdown underutilized virtual machines
---
{
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "d472fb24-d23c-480f-896f-b3095d5bd868",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.ClassicCompute/virtualMachines",
  "recommendationFriendlyName": "LowUsageVmClassic",
  "recommendationMetadataState": "Disabled",
  "portalFeatures": [],
  "owner": {
    "email": "cloudfit@microsoft.com",
    "icm": {
      "routingId": "MDM://CloudFit/FileAllIncidentsHere",
      "service": "CloudFit",
      "team": "FileAllIncidentsHere"
    },
    "serviceTreeId": "eb7e1413-a83d-460e-9e1d-0eef53d38698"
  },
  "recommendationTimeToLive": 86400,
  "version": 3.0,
  "learnMoreLink": "https://aka.ms/aa_lowusagerec_learnmore",
  "description": "Right-size or shutdown underutilized virtual machines",
  "longDescription": "We've analyzed the usage patterns of your virtual machine over the past 7 days, and identified virtual machines with low usage. While certain scenarios can result in low utilization by design, you can often save money by managing the size and number of virtual machines.",
  "potentialBenefits": "savings per year",
  "actions": [
    {
      "actionId": "682c31f3-f0e3-49c1-b3fc-df0b88ba094a",
      "description": "Shut down the virtual machine",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      },
      "condition": "targetSku == \"Shutdown\""
    },
    {
      "actionId": "7bfdedec-390e-4198-8514-a1b9828a34fb",
      "description": "Resize {currentSku} to {targetSku}",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}",
        "menuid": "size"
      },
      "condition": "targetSku != \"Shutdown\""
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "1e2e1193-ec3f-4169-a5ba-f2d65328f61b",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Shut down or resize your virtual machine",
  "additionalColumns": [],
  "ingestionClientIdentities": [
    "CN=metricsclient.geneva.core.microsoft.scloud"
  ],
  "tip": "You can optimize underutilized virtual machines to reduce your monthly Azure spend.",
  "costSavingInfo": "*You can save up to the stated amount and your actual savings may vary."
}
---
