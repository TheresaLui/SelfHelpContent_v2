<properties
    pageTitle="Scale the PostgreSQL server to higher SKU"
    description="Scale the PostgreSQL server to higher SKU"
    authors="manishku"
    ms.author="kummanish"
    articleId="bd109fe8-a2cf-415a-adcb-5e9f9fc1d3c0_Fairfax"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Fairfax"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Scale the PostgreSQL server to higher SKU
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "bd109fe8-a2cf-415a-adcb-5e9f9fc1d3c0",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureusg.kusto.usgovcloudapi.net').database('FairFax').GetPostgreSqlConnectionRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DbForPostgresql/servers",
  "recommendationFriendlyName": "OrcasPostgreSqlConcurrentConnection",
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
  "learnMoreLink": "https://aka.ms/postgresqlconnectionlimits",
  "description": "Scale the PostgreSQL server to higher SKU",
  "longDescription": "Our internal telemetry shows that the server may be unable to support the connection requests because of the maximum supported connections for the given SKU. This may result in a large number of failed connections requests which adversly affect the the performance. To improve performance, we recommend to move to higher memory SKU by increasing vCore or switching to Memory-Optimized SKUs.",
  "potentialBenefits": "Improve query performance by allowing more concurrent connections",
  "actions": [
    {
      "actionId": "5f7b1e08-edfe-420e-9240-8fd0d88b9d28",
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
      "actionId": "30f0ddb6-e1d6-4102-b2f2-8e1cad01b678",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Scale the PostgreSQL server to higher SKU",
  "additionalColumns": [],
  "tip": "You can improve the query performance of your PostgreSQL database by scaling your server to a higher SKU."
}
---
