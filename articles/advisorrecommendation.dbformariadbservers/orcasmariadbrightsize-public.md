<properties
    pageTitle="Right-size underutilized MariaDB servers"
    description="Right size the MariaDB server vCores based on the utilization telemetry."
    authors="manishku"
    ms.author="kummanish"
    articleId="2af11142-942e-45c1-8ce8-d9d2df25aae9_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public,Usnat, ussec"
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
    "schemaVersion": 2.0,
    "dataSource": "SAS"
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
  "ingestionClientIdentities": [
    "49ebada5-bdc9-4c9b-826c-3cb789357c5d"
  ],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://aka.ms/mariadbpricing",
  "description": "Right-size underutilized MariaDB servers",
  "longDescription": "Our internal telemetry shows that the MariaDB database server resources has been underutilized for an extended period of time over the last 7 days. Low resource utilization results in unwanted expenditure which can be fixed without significant performance impact. To reduce your costs and efficiently manage your resources, we recommend reducing the compute size (vCores) by half.",
  "potentialBenefits": "Reduce cost by right-sizing the MariaDB server",
  "actions": [
    {
      "actionId": "9920d56d-3bf5-4ed3-b980-4162e558925f",
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
      "actionId": "b3720c34-374e-4f36-8c43-7e60862c5798",
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
