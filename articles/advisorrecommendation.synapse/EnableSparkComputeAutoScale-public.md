<properties
    pageTitle="Enable autopause and autoscale properties on spark compute"
    description="Enable autopause and autoscale properties on spark compute"
    authors="srthatip"
    ms.author="srthatip"
    articleId="018da770-932b-4fce-92e4-efc51f411279_public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureData_AzureSQLDB_DataWarehouse"
/>

# Consider enabling Autoscale feature on spark pool for better performance
---
{
  "recommendationOfferingId": "bfd090af-60cd-4f06-9a20-84224a93df41",
  "recommendationOfferingName": "Azure Synapse Analytics",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "018da770-932b-4fce-92e4-efc51f411279",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('analytics365prod.kusto.windows.net').database('Analytics365PROD').synapse_advisor_EnableAutoScaleAutoPause",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
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
  "version": 2.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-autoscale",
  "description": "Consider enabling Autoscale feature on spark pool.",
  "longDescription": "Apache Spark for Azure Synapse Analytics pool's Autoscale feature automatically scales the number of nodes in a cluster instance up and down. During the creation of a new Apache Spark for Azure Synapse Analytics pool, a minimum and maximum number of nodes can be set when Autoscale is selected. Autoscale then monitors the resource requirements of the load and scales the number of nodes up or down. There's no additional charge for this feature.",
  "potentialBenefits": "Enabling Autoscale comes at 0 cost and will help increase load throughput and improve performance",
  "actions": [
    {
      "actionId": "79444364-79be-4656-99b9-9919daedfb96",
      "description": "Consider enabling Autoscale feature on spark pool",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/synapse-analytics/spark/apache-spark-autoscale"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "54d77cf5-16c2-4cfe-b4be-2af207f1ed15",
      "actionType": "Blade",
      "extensionName": "SynapseworkspaceExtension",
      "bladeName": "SynapseworkspaceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Consider enabling Autoscale feature on spark pool",
  "additionalColumns": [
	{
		"name": "SparkPool",
		"title": "Spark Compute"
	}
  ],
  "tip": "You can improve load throughput, performance by enabling autoscale."

}
---
