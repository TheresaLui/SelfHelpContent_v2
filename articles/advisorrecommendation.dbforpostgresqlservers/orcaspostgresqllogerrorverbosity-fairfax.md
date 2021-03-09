<properties
    pageTitle="Improve PostgreSQL log performance"
    description="Improve PostgreSQL log performance"
    authors="alau"
    ms.author="alau-ms"
    articleId="661dd0c2-5d39-4cfb-ba57-59808643e36d_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Change log_error_verbosity to improve PostgreSQL database performance
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "661dd0c2-5d39-4cfb-ba57-59808643e36d",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureusg.kusto.usgovcloudapi.net').database('FairFax').GetPostgreSqlLogErrorVerbosityRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.DbForPostgresql/servers",
  "recommendationFriendlyName": "OrcasPostgreSqlLogErrorVerbosity",
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
  "ingestionClientIdentities": [
    "49ebada5-bdc9-4c9b-826c-3cb789357c5d"
  ],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/azure_postgresql_log_settings",
  "description": "Improve PostgreSQL log performance",
  "longDescription": "Our internal telemetry indicates that your PostgreSQL server has been configured to output VERBOSE error logs. This can be useful for troubleshooting your database, but it can also result in reduced database performance. To improve performance, we recommend that you change the log_error_verbosity parameter to the DEFAULT setting.",
  "potentialBenefits": "Improve database performance by changing the log_error_verbosity parameter to the DEFAULT setting",
  "actions": [
    {
      "actionId": "00a13034-5a4f-4c5a-927c-7b4c4a4e8a74",
      "description": "Set log_error_verbosity to DEFAULT",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "PostgreSqlServerParametersBlade",
      "metadata": {
        "resourceId": "{resourceId}"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "29bc2e15-bb85-455e-bb68-e668378e6590",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Adjust server parameter: log_error_verbosity",
  "additionalColumns": [],
  "tip": "You can improve your PostgreSQL database performance by changing your log_error_verbosity setting."
}
---