<properties
    pageTitle="Right-size underutilized MariaDB servers"
    description="Right size the MariaDB server vCores based on the utilization telemetry."
    authors="ambhatna"
    ms.author="ambhatna"
    articleId="2af11142-942e-45c1-8ce8-d9d2df25aae9_USSec"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="ussec"
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
    "streamNamespace": "cluster('https://sqlazureussece.usseceast.kusto.core.microsoft.scloud').database('sqlazure1').GetMariaDBRightSizeRecommendations",
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
      "actionId": "e9702aa5-5510-4d67-8ea9-80699003f4c3",
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
      "actionId": "9bc0a051-e0de-49f1-88aa-f3db1e997d08",
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
