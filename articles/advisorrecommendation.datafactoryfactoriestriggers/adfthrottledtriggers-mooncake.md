<properties
    pageTitle="Review your throttled Data Factory Triggers"
    description="Review your throttled Data Factory Triggers"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="eb4f67d2-2440-4d58-bec7-6de73cc5ba75_MoonCake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="MoonCake"
	ownershipId="AzureData_DataFactory"
/>
# Review your throttled Data Factory Triggers
---
{
  "recommendationOfferingId": "d5fbb83d-baa0-4d89-82ca-73476c963144",
  "recommendationOfferingName": "Data Factory",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "eb4f67d2-2440-4d58-bec7-6de73cc5ba75",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "cluster('https://adfmc.kusto.chinacloudapi.cn').database('azuredatafactorymc').AdvisorThrottledTriggerEvents",
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DataFactory/factories/triggers",
  "recommendationFriendlyName": "ADFThrottledTriggers",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "adfengineering@microsoft.com",
    "icm": {
      "routingId": "AIMS://ADFV2_PROD_SEV3",
      "service": "Azure Data Factory",
      "team": "ADF V2 Orchestration"
    },
    "serviceTreeId": "f76de4a1-629f-4651-9d76-1d7b56544f3c"
  },
  "ingestionClientIdentities": [],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/adf-create-event-trigger",
  "description": "Review your throttled Data Factory Triggers",
  "longDescription": "A high volume of throttling has been detected in an event-based trigger that runs in your Data Factory resource. This is causing your pipeline runs to drop from the run queue. Review the trigger definition to resolve issues and increase performance.",
  "potentialBenefits": "Ensure better performance by reviewing and editing your event-based trigger definition",
  "actions": [
    {
      "actionId": "c30644ac-806b-40d5-8654-4d1bccf5f5ff",
      "description": "Review and edit your event-based trigger",
      "actionType": "Document",
      "documentLink": "{externalLink}"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "3b881624-7744-448f-80c6-76aa4e819107",
      "description": "{triggerName}",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}",
        "triggerName": "{triggerName}"
      }
    }
  },
  "displayLabel": "Review your throttled Data Factory Triggers",
  "additionalColumns": [
    {
      "name": "dataFactoryName",
      "title": "Data Factory Name"
    }
  ]
}
---
