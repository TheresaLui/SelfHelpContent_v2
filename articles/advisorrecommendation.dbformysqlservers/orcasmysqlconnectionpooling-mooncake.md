<properties
    pageTitle="Improve MySQL connection management"
    description="Improve MySQL connection management"
    authors="ambhatna"
    ms.author="ambhatna"
    articleId="f62ef41c-2cdb-4f4e-9dc9-a391c579b0fb_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Improve MySQL connection management
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "f62ef41c-2cdb-4f4e-9dc9-a391c579b0fb",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazurechi2.chinanorth2.kusto.chinacloudapi.cn').database('MoonCake').GetMySqlConnectionPoolingRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.DbForMysql/servers",
  "recommendationFriendlyName": "OrcasMySQLConnectionPooling",
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
  "learnMoreLink": "https://aka.ms/azure_mysql_connection_pooling",
  "description": "Improve MySQL connection management",
  "longDescription": "Our internal telemetry indicates that your application connecting to MySQL server may not be managing connections efficiently. This may result in unnecessary resource consumption and overall higher application latency. To improve connection management, we recommend that you reduce the number of short-lived connections and eliminate unnecessary idle connections. This can be done by configuring a server side connection-pooler, such as ProxySQL.",
  "potentialBenefits": "Improve performance by reducing overhead associated with short-lived and idle database connections",
  "actions": [
    {
      "actionId": "9eb9264c-85be-4567-8010-1902f10f04a1",
      "description": "Configuring Connection Pooling using ProxySQL",
      "actionType": "Document",
      "documentLink": "https://aka.ms/azure_mysql_proxysql"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "d4b519bf-615b-4d4b-8f3d-08425af2283e",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Improve MySQL connection management",
  "additionalColumns": [],
  "tip": "You can manage your MySQL database connections more efficiently by configuring a connection pooler, such as ProxySQL."
}
---
