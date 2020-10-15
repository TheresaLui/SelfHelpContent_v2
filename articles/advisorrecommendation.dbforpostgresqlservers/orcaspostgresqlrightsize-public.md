<properties
    pageTitle="Right-size underutilized PostgreSQL servers"
    description="Right size the PostgreSQL server vCores based on the utilization telemetry."
    authors="manishku"
    ms.author="kummanish"
    articleId="38f4a461-1543-4089-854c-90e7edf37707_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public,USNat,USSec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Reduce the resource cost for Azure Database for PostgreSQL
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "38f4a461-1543-4089-854c-90e7edf37707",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DbForPostgresql/servers",
  "recommendationFriendlyName": "OrcasPostgreSqlCpuRightSize",
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
  "version": 2.0,
  "learnMoreLink": "https://aka.ms/postgresqlpricing",
  "description": "Right-size underutilized PostgreSQL servers",
  "longDescription": "Our internal telemetry shows that the PostgreSQL database server resources has been underutilized for an extended period of time over the last 7 days. Low resource utilization results in unwanted expenditure which can be fixed without significant performance impact. To reduce your costs and efficiently manage your resources, we recommend reducing the compute size (vCores) by half.",
  "potentialBenefits": "Reduce cost by right-sizing the PostgreSQL server",
  "actions": [
    {
      "actionId": "5c1e3ad5-2295-407c-9de1-ba585cfeb0b3",
      "description": "Right-size underutilized PostgreSQL servers",
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
      "actionId": "3278789a-ade7-4867-93c6-9ba250035ca5",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Right-size underutilized PostgreSQL server",
  "additionalColumns": [],
  "tip": "You can improve the overall resource spend for your Azure Database for PostgreSQL by scaling down the compute resources by half."
}
---
