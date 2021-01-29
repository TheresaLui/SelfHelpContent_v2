<properties
    pageTitle="Enable autoscale feature on spark compute"
    description="Enable autoscale feature on spark compute"
    authors="srthatip"
    ms.author="srthatip"
    articleId="00b1ef72-4d0f-4452-a6a8-1df5397172d6_mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="AzureData_SynapseAnalytics"
/>

# Consider enabling autoscale feature on spark compute
---
{
  "recommendationOfferingId": "36bdbad1-7a98-45b6-bba9-5de8c197f991",
  "recommendationOfferingName": "Azure Synapse Analytics",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "00b1ef72-4d0f-4452-a6a8-1df5397172d6",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('analytics365prod.chinanorth2.kusto.chinacloudapi.cn').database('Analytics365PROD').synapse_advisor_EnableAutoScale",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Low",
  "recommendationResourceType": "Microsoft.Synapse/workspaces",
  "recommendationFriendlyName": "EnableSynapseSparkComputeAutoScaleGuidance",
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
  "learnMoreLink": "https://aka.ms/EnableSynapseSparkComputeAutoScaleGuidance",
  "description": "Consider enabling autoscale feature on spark compute.",
  "longDescription": "Apache Spark for Azure Synapse Analytics pool's Autoscale feature automatically scales the number of nodes in a cluster instance up and down. During the creation of a new Apache Spark for Azure Synapse Analytics pool, a minimum and maximum number of nodes can be set when Autoscale is selected. Autoscale then monitors the resource requirements of the load and scales the number of nodes up or down. There's no additional charge for this feature.",
  "potentialBenefits": "The Autoscale feature monitors resource requirements and automatically scales the number of nodes up and down to meet the compute and memory requirements, thereby optimizing costs from unused resources.",
  "actions": [
    {
      "actionId": "79444364-79be-4656-99b9-9919daedfb96",
      "description": "Consider enabling autoscale feature on spark compute",
      "actionType": "Document",
      "documentLink": "https://aka.ms/EnableSynapseSparkComputeAutoScaleGuidance"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "54d77cf5-16c2-4cfe-b4be-2af207f1ed15",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Consider enabling autoscale feature on spark compute",
  "additionalColumns": [
	{
		"name": "sparkPool",
		"title": "Spark Compute"
	}
  ],
  "tip": "Enabling autoscale comes at 0 cost and will reduce job failures."

}
---
