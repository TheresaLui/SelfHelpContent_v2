<properties
    pageTitle="Improve MySQL connection latency"
    description="Improve MySQL connection latency"
    authors="alau"
    ms.author="alau-ms"
    articleId="2cbca084-4e80-4720-a7fe-dc8c3074e8ca_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Improve MySQL connection latency
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "2cbca084-4e80-4720-a7fe-dc8c3074e8ca",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazurechi2.chinanorth2.kusto.chinacloudapi.cn').database('MoonCake').GetMySqlRedirectionRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.DbForMysql/servers",
  "recommendationFriendlyName": "OrcasMySQLConnectionRedirection",
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
  "learnMoreLink": "https://aka.ms/azure_mysql_connection_redirection",
  "description": "Improve MySQL connection latency",
  "longDescription": "Our internal telemetry indicates that your application connecting to MySQL server may not be managing connections efficiently. This may result in higher application latency. To improve connection latency, we recommend that you enable connection redirection. This can be done by enabling the connection redirection feature of the PHP driver.",
  "potentialBenefits": "Reduce network latency between client applications",
  "actions": [
    {
      "actionId": "e23dab88-745f-4220-93a9-346453403f42",
      "description": "Configure the redirect_enabled parameter to ON to allow connections with redirection mode",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "MySqlServerParametersBlade",
      "metadata": {
        "resourceId": "{resourceId}"
      }
    },
    {
      "actionId": "366acc4e-4632-48b9-953d-139ec3e91290",
      "description": "Connect to Azure Database for MySQL with redirection",
      "actionType": "Document",
      "documentLink": "https://aka.ms/azure_mysql_connection_redirection"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "550d964a-4fc0-4b59-9756-42797cd68a64",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Improve MySQL connection latency",
  "additionalColumns": [],
  "tip": "You can manage your MySQL database connections more efficiently by enabling connection redirection."
}
---
