<properties
    pageTitle="Upgrade your Azure Cosmos DB Spark Connector to the latest version from Maven"
    description="Upgrade your Azure Cosmos DB Spark Connector to the latest version from Maven"
    authors="rnagpal"
    ms.author="rnagpal"
    articleId="c38d8bf8-d7a7-4480-ad49-15e52bf4481a_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="AzureData_AzureCosmosDB"
/>
# Upgrade your Azure Cosmos DB Spark Connector to the latest version from Maven
---
{
  "recommendationOfferingId": "86ec4e3b-1865-4240-89f6-c2f3553df5ac",
  "recommendationOfferingName": "Azure Cosmos DB",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "c38d8bf8-d7a7-4480-ad49-15e52bf4481a",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://cdbfairfax.kusto.usgovcloudapi.net').database('LiveSite').OldSparkConnector",
    "dataSource": "Kusto",
    "refreshInterval": "0.12:00:00"
  },
  "recommendationCategory": "HighAvailability",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "microsoft.documentdb/databaseaccounts",
  "recommendationFriendlyName": "CosmosDbUpgradeSparkConnector",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "cosmosnotifications@microsoft.com",
    "icm": {
      "routingId": "mdm://adspartner/CosmosDb",
      "service": "Azure Cosmos DB",
      "team": "Supportability"
    },
    "serviceTreeId": "724c33bf-1ab8-4691-adb1-0e61932919c2"
  },
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/cosmosdb/spark-connector",
  "description": "Upgrade your Azure Cosmos DB Spark Connector to the latest version from Maven",
  "longDescription": "Your Azure Cosmos DB account is using an old version of the Cosmos DB Spark connector. We recommend upgrading to the latest version from Maven for latest fixes, performance improvements, and new feature capabilities.",
  "potentialBenefits": "Improved reliability, performance, and new feature capabilities",
  "displayLabel": "Upgrade your Azure Cosmos DB Spark Connector to the latest version from Maven",
  "additionalColumns": [
    {
      "name": "LatestVersion",
      "title": "Latest Version"
    }
  ],
  "actions": [
    {
      "actionId": "3ff4f4ee-ca4f-4d08-976c-de7c2bfd6a98",
      "description": "Upgrade your Spark Connector",
      "actionType": "Document",
      "documentLink": "https://aka.ms/cosmosdb/spark-connector"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "1f811f71-76fd-4946-8d5f-5ffedf9849ab",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  }
}
---
