<properties
    pageTitle="Rebalance data in Hyperscale (Citus) server group to distribute workload among worker nodes more evenly"
    description="Rebalance data in Hyperscale (Citus) server group to distribute workload among worker nodes more evenly"
    authors="buvelio"
    ms.author="buvelio"
    articleId="426292db-b3e8-46f6-ad3e-d46753943afb_Mooncake"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Mooncake"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Rebalance data in Hyperscale (Citus) server group to distribute workload among worker nodes more evenly
---
{
  "recommendationOfferingId": "ace8d53f-889a-488c-9cc9-d31fb4bbc84a",
  "recommendationOfferingName": "Open Source RDBMS (Orcas)",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "426292db-b3e8-46f6-ad3e-d46753943afb",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazurechi2.chinanorth2.kusto.chinacloudapi.cn').database('MoonCake').GetCitusShardRebalancerRecommendations",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "24:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.DbForPostgresql/serverGroups",
  "recommendationFriendlyName": "OrcasPostgreSqlCitusRebalanceData",
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
  "learnMoreLink": "https://go.microsoft.com/fwlink/?linkid=2148869",
  "description": "Rebalance data in Hyperscale (Citus) server group to distribute workload among worker nodes more evenly",
  "longDescription": "It looks like the data is not well balanced between worker nodes in this Hyperscale (Citus) server group. In order to use each worker node of the Hyperscale (Citus) server group effectively rebalance data in this server group.",
  "potentialBenefits": "Get the most of Hyperscale (Citus) by utilizing resources of each node more evenly",
  "actions": [
    {
      "actionId": "5481e6c6-5938-4cea-8585-e5543cd7b664",
      "description": "Rebalance data in Hyperscale (Citus) server group to distribute workload among worker nodes more evenly",
      "actionType": "Document",
      "documentLink": "https://go.microsoft.com/fwlink/?linkid=2148869"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "1371b337-a3ef-4734-9622-6f9a9cef9e35",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Rebalance data in Hyperscale (Citus) server group to distribute workload among worker nodes more evenly",
  "additionalColumns": []
}
---