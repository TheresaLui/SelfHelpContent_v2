<properties
    pageTitle="Enable autopause feature on spark compute"
    description="Enable autopause feature on spark compute"
    authors="srthatip"
    ms.author="srthatip"
    articleId="afdf4c1a-e46b-4817-a5d6-4b9909f58e2a_mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="AzureData_SynapseAnalytics"
/>

# Consider enabling autopause feature on spark compute
---
{
  "recommendationOfferingId": "36bdbad1-7a98-45b6-bba9-5de8c197f991",
  "recommendationOfferingName": "Azure Synapse Analytics",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "afdf4c1a-e46b-4817-a5d6-4b9909f58e2a",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('analytics365prod.chinanorth2.kusto.chinacloudapi.cn').database('Analytics365PROD').synapse_advisor_EnableAutoPause",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Low",
  "recommendationResourceType": "Microsoft.Synapse/workspaces",
  "recommendationFriendlyName": "EnableSynapseSparkComputeAutoPauseGuidance",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "a365rp@microsoft.com",
    "icm": {
      "routingId": "mdm://adspartner/AzureSynapsePlateform/SynapseProvider",
      "service": "Azure Synapse Platform Service",
      "team": "Synapse Resource Provider"
    },
    "serviceTreeId": "c0ee70d5-102d-438c-8858-795b92dc0f99"
  },
  "ingestionClientIdentities": [ ],
  "version": 3.0,
  "learnMoreLink": "https://aka.ms/EnableSynapseSparkComputeAutoPauseGuidance",
  "description": "Consider enabling autopause feature on spark compute.",
  "longDescription": "Auto-pause releases and shuts down unused compute resources after a set idle period of inactivity",
  "potentialBenefits": "Auto-pause releases and shuts down unused compute resources after a set idle period of inactivity",
  "actions": [
    {
      "actionId": "79444364-79be-4656-99b9-9919daedfb36",
      "description": "Consider enabling autopause feature on spark compute",
      "actionType": "Document",
      "documentLink": "https://aka.ms/EnableSynapseSparkComputeAutoPauseGuidance"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "54d77cf5-16c2-4cfe-b4be-2af207f1ed25",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Consider enabling autopause feature on spark compute",
  "additionalColumns": [
	{
		"name": "sparkPool",
		"title": "Spark Compute"
	}
  ],
  "tip": "Auto-pause releases and shuts down unused compute resources after a set idle period of inactivity."

}
---
