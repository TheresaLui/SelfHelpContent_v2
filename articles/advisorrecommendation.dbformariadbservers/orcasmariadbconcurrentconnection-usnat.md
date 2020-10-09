<properties
    pageTitle="Scale the MariaDB server to higher SKU"
    description="Scale the MariaDB server to higher SKU"
    authors="manishku"
    ms.author="kummanish"
    articleId="860d2d5d-7934-4ccb-a34a-577adf3022a6_USNat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USNat"
    ownershipId="AzureData_AzureDatabaseforMariaDB"
/>
# Scale the MariaDB server to higher SKU
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "860d2d5d-7934-4ccb-a34a-577adf3022a6",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureusnate.usnateast.kusto.core.eaglex.ic.gov').database('sqlazure1').GetMariaDBConnectionRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DbForMariadb/servers",
  "recommendationFriendlyName": "OrcasMariaDbConcurrentConnection",
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
  "learnMoreLink": "https://aka.ms/mariadbconnectionlimits",
  "description": "Scale the MariaDB server to higher SKU",
  "longDescription": "Our internal telemetry shows that the server may be unable to support the connection requests because of the maximum supported connections for the given SKU. This may result in a large number of failed connections requests which adversly affect the the performance. To improve performance, we recommend to move to higher memory SKU by increasing vCore or switching to Memory-Optimized SKUs.",
  "potentialBenefits": "Improve query performance by allowing more concurrent connections",
  "actions": [
    {
      "actionId": "ef80ca3e-819f-40eb-805f-9609a1001b24",
      "description": "Increase vCores or switch to Memory Optimized pricing tier",
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
      "actionId": "58da2a8a-2142-410b-a006-177d4a20063b",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Scale the MariaDB server to higher SKU",
  "additionalColumns": [],
  "tip": "You can improve the query performance of your MariaDB database by scaling your server to a higher SKU."
}
---
