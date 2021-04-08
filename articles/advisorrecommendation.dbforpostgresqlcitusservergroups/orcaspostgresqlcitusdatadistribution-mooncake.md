<properties
    pageTitle="Distribute data in server group to distribute workload among nodes"
    description="Distribute data in server group to distribute workload among nodes"
    authors="buvelio"
    ms.author="buvelio"
    articleId="c3c74c9e-e241-496c-be3f-57a2797aa91f_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Distribute data in server group to distribute workload among nodes
---
{
  "recommendationOfferingId": " ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": " Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "c3c74c9e-e241-496c-be3f-57a2797aa91f",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazurechi2.chinanorth2.kusto.chinacloudapi.cn').database('MoonCake').GetCitusDataDistributionRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "24:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.DbForPostgresql/serverGroups",
  "recommendationFriendlyName": "OrcasPostgreSqlCitusDistributeData",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "CitusOnAzure@service.microsoft.com",
    "icm": {
      "routingId": "AIMS://AZURE OSS DATABASES/Open Source RDBMS",
      "service": "Azure OSS Databases",
      "team": "Open Source RDBMS - Breadth DRI"
    },
    "serviceTreeId": "461f15e6-e9f5-404e-b873-fcb306e8837d"
  },
  "ingestionClientIdentities": [
    "49ebada5-bdc9-4c9b-826c-3cb789357c5d"
  ],
  "recommendationTimeToLive": 86400,
  "version": 1.0,
  "learnMoreLink": "https://go.microsoft.com/fwlink/?linkid=2135201",
  "description": "Distribute data in server group to distribute workload among nodes",
  "longDescription": "It looks like the data has not been distributed in this server group but stays on the coordinator. For full Hyperscale (Citus) benefits distribute data on worker nodes in this server group.",
  "potentialBenefits": "Improve query performance by utilizing resource of each node in the server group",
  "actions": [
    {
      "actionId": "2f16705d-f955-4be1-841f-35493d206a8e",
      "description": "Distribute data in server group to distribute workload among nodes",
      "actionType": "Document",
      "documentLink": "https://go.microsoft.com/fwlink/?linkid=2135201"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "a64c6a85-cbe7-4160-9c80-ae04ba9fb1d1",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Distribute data in server group to distribute workload among nodes",
  "additionalColumns": []
}
---