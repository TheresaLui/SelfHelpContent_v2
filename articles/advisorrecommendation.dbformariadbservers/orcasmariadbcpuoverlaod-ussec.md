<properties
    pageTitle="Increase the MariaDB server vCores"
    description="Increase the MariaDB server vCores"
    authors="ambhatna"
    ms.author="ambhatna"
    articleId="a5f888e3-8cf4-4491-b2ba-b120e14eb7ce_USSec"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="ussec"
    ownershipId="AzureData_AzureDatabaseforMariaDB"
/>
# Increase the MariaDB server vCores
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "a5f888e3-8cf4-4491-b2ba-b120e14eb7ce",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureussece.usseceast.kusto.core.microsoft.scloud').database('sqlazure1').GetMariaDBCpuRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DbForMariadb/servers",
  "recommendationFriendlyName": "OrcasMariaDbCpuOverlaod",
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
  "description": "Increase the MariaDB server vCores",
  "longDescription": "Our internal telemetry shows that the CPU has been running under high utilization for an extended period of time over the last 7 days. High CPU utilization may lead to slow query performance. To improve performance, we recommend moving to a larger compute size.",
  "potentialBenefits": "Improve query performance by reducing CPU pressure",
  "actions": [
    {
      "actionId": "e5de7bbe-a0c6-4b2b-a443-2479fe9f4be6",
      "description": "Increase your server's CPU vCores",
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
      "actionId": "bd499726-5dd9-4a68-be71-d97c8b9308bc",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Increase the MariaDB server vCores",
  "additionalColumns": [],
  "tip": "You can improve the query performance of your MariaDB database by increasing the server vCores."
}
---
