<properties
    pageTitle="Right-size underutilized MySQL servers"
    description="Right size the MySQL server vCores based on the utilization telemetry."
    authors="manishku"
    ms.author="kummanish"
    articleId="7e76e54f-7978-4d48-9ab9-a4da5b7c69a3_USNat"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USNat"
	  ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Reduce the resource cost for Azure Database for MySQL
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "7e76e54f-7978-4d48-9ab9-a4da5b7c69a3",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureusnate.usnateast.kusto.core.eaglex.ic.gov').database('sqlazure1').GetMySqlRightSizeRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Cost",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.DbForMysql/servers",
  "recommendationFriendlyName": "OrcasMySQLCpuRightSize",
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
  "learnMoreLink": "https://aka.ms/mysqlpricing",
  "description": "Right-size underutilized MySQL servers",
  "longDescription": "Our internal telemetry shows that the MySQL database server resources has been underutilized for an extended period of time over the last 7 days. Low resource utilization results in unwanted expenditure which can be fixed without significant performance impact. To reduce your costs and efficiently manage your resources, we recommend reducing the compute size (vCores) by half.",
  "potentialBenefits": "Reduce cost by right-sizing the MySQL server",
  "actions": [
    {
      "actionId": "b460b306-706f-4fe4-8a61-8eb8e10013a6",
      "description": "Right-size underutilized MySQL servers",
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
      "actionId": "27a31aaf-aff5-4211-b2eb-b10b6d17694a",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Right-size underutilized MySQL server",
  "additionalColumns": [],
  "tip": "You can improve the overall resource spend for your Azure Database for MySQL by scaling down the compute resources by half."
}
---
