<properties
    pageTitle="Scale the storage limit for MySQL server"
    description="Scale the storage limit for MySQL server"
    authors="manishku"
    ms.author="kummanish"
    articleId="c0576597-4910-48b5-9828-5b3a99190b82_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Scale the storage limit for MySQL server
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "c0576597-4910-48b5-9828-5b3a99190b82",
  "dataSourceMetadata": {
    "schemaVersion": 2.0,
    "dataSource": "SAS"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.DbForMysql/servers",
  "recommendationFriendlyName": "OrcasMySQLStorageLimit",
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
  "learnMoreLink": "https://aka.ms/mysqlstoragelimits",
  "description": "Scale the storage limit for MySQL server",
  "longDescription": "Our internal telemetry shows that the server may be constrained because it is approaching limits for the currently provisioned storage values. This may result in degraded performance or in the server being moved to read-only mode. To ensure continued performance, we recommend increasing the provisioned storage amount or turning ON the \"Auto-Growth\" feature for automatic storage increases",
  "potentialBenefits": "Improve query performance by allocating larger storage for the server",
  "actions": [
    {
      "actionId": "4ac97246-dbf9-4e90-a688-d4d6bfe90a30",
      "description": "Increase Storage for your MySQL Server",
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
      "actionId": "98fd94e3-420b-4d87-99b7-7289905a25dd",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Increase the Server Storage limit",
  "additionalColumns": []
}
---