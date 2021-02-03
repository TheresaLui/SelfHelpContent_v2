<properties
    pageTitle="Delete failing ADF pipelines"
    description="Delete failing ADF pipelines"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="f6e3ad9c-5d58-48ba-b06b-ebffba60dd18_MoonCake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="MoonCake"
	ownershipId="AzureData_DataFactory"
/>
# Delete failing ADF pipelines
---
{
  "recommendationOfferingId": "d5fbb83d-baa0-4d89-82ca-73476c963144",
  "recommendationOfferingName": "Data Factory",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "f6e3ad9c-5d58-48ba-b06b-ebffba60dd18",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "streamNamespace": "cluster('https://adfmc.kusto.chinacloudapi.cn').database('azuredatafactorymc').AdvisorRepeatedlyFailingPipelines",
    "dataSource": "Kusto",
    "refreshInterval": "08:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DataFactory/factories/pipelines",
  "recommendationFriendlyName": "ADFFailingPipelines",
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
  "learnMoreLink": "https://aka.ms/aa_advisor_adfpipeline",
  "description": "Delete failing ADF pipelines",
  "longDescription": "Repeatedly failing pipelines have been detected in your Azure Data Factory resource. Know that you are being billed for them even though they are not serving you while failing. Review them to resolve issues or delete failing pipelines that are no longer needed to save on costs",
  "potentialBenefits": "Reduce billing costs by addressing issues with or deleting your failing Data Factory pipelines",
  "actions": [
    {
      "actionId": "def98a4f-1d26-4624-860e-500353985370",
      "description": "Review or delete your repeatedly failing pipelines",
      "actionType": "Document",
      "documentLink": "{externalLink}"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "a2d2f9da-fcd0-4ed9-9931-f2c6f0e52c21",
      "description": "{pipelineName}",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}",
        "pipelineName": "{pipelineName}"
      }
    }
  },
  "displayLabel": "Delete failing ADF pipelines",
  "additionalColumns": [
    {
      "name": "dataFactoryName",
      "title": "Data factory Name"
    }
  ]
}
---
