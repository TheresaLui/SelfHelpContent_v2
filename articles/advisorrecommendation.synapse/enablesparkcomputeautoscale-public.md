<properties
    pageTitle="Enable autoscale properties on spark compute"
    description="Enable autoscale properties on spark compute"
    authors="srthatip"
    ms.author="srthatip"
    articleId="018da770-932b-4fce-92e4-efc51f411279_public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureData_AzureSQLDB_DataWarehouse"
/>

# Consider enabling autoscale feature on spark compute for better performance
---
{
  "recommendationOfferingId": "36bdbad1-7a98-45b6-bba9-5de8c197f991",
  "recommendationOfferingName": "Azure Synapse Analytics",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "018da770-932b-4fce-92e4-efc51f411279",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('analytics365prod.kusto.windows.net').database('Analytics365PROD').synapse_advisor_EnableAutoScaleAutoPause",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Low",
  "recommendationResourceType": "Microsoft.Synapse/workspaces",
  "recommendationFriendlyName": "EnableAutoScaleAutoPauseGuidance",
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
  "version": 7.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-autoscale",
  "description": "Consider enabling autoscale feature on spark compute.",
  "longDescription": "Apache Spark for Azure Synapse Analytics pool's Autoscale feature automatically scales the number of nodes in a cluster instance up and down. During the creation of a new Apache Spark for Azure Synapse Analytics pool, a minimum and maximum number of nodes can be set when Autoscale is selected. Autoscale then monitors the resource requirements of the load and scales the number of nodes up or down. There's no additional charge for this feature.",
  "potentialBenefits": "Enabling autoscale comes at 0 cost and will reduce job failures.",
  "actions": [
    {
      "actionId": "79444364-79be-4656-99b9-9919daedfb96",
      "description": "Consider enabling autoscale feature on spark compute",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-autoscale"
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
