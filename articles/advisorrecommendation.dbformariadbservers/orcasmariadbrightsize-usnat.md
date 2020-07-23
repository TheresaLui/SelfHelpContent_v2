<properties
    pageTitle="Right-size underutilized MariaDB servers"
    description="Right size the MariaDB server vCores based on the utilization telemetry."
    authors="manishku"
    ms.author="kummanish"
    articleId="2af11142-942e-45c1-8ce8-d9d2df25aae9_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USNat"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>
# Decrease the MariaDB server vCores
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "2af11142-942e-45c1-8ce8-d9d2df25aae9",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureusg.kusto.usgovcloudapi.net').database('FairFax').GetMariaDBRightSizeRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DbForMariadb/servers",
  "recommendationFriendlyName": "OrcasMariaDbCpuRightSize",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "orcasql-livesite@service.microsoft.com",
    "icm": {
      "routingId": "AIMS://AZURE OSS DATABASES/Open Source RDBMS",
      "service": "Azure OSS Databases",
      "team": "Open Source RDBMS (Project OrcaSQL)"
    },
    "serviceTreeId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a"
  },
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/mariadbpricing",
  "description": "Right-size underutilized MariaDB servers",
  "longDescription": "Our internal telemetry shows that the MariaDB database server resources has been underutilized for an extended period of time over the last 7 days. Low resource utilization results in unwanted expenditure which can be fixed without significant performance impact. To reduce your costs and efficiently manage your resources, we recommend reducing the compute size (vCores) by half.",
  "potentialBenefits": "Reduce cost by right-sizing the MariaDB server",
  "actions": [
    {
      "actionId": "c4a0f43f-8b9f-450e-b3ba-d7f20f1a567b",
      "description": "Right-size underutilized MariaDB servers",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}",
        "menuid": "pricingTier"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "15117dd0-e036-4713-9a2a-559baa46775f",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Right-size underutilized MariaDB server",
  "additionalColumns": [],
  "tip": "You can improve the overall resource spend for your Azure Database for MariaDB by scaling down the compute resources by half."
}
---
