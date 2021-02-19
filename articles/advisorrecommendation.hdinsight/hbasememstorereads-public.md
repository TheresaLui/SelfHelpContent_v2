<properties
    pageTitle="HBaseMemstoreReads"
    description="HBase reads on latest data"
	authors="ramvasu"
    ms.author="ramvasu"
    articleId="2a570d9c-79a9-4570-99ee-eb90905124b1_Public"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="Public, usnat, ussec"
    ownershipId="AzureData_HDInsight"
/>
# Reads happening on latest data
---
{
  "recommendationOfferingId": "83bd2e45-415f-4783-97de-aef7d97ffa97",
  "recommendationOfferingName": "HDInsight",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "80c1538d-5962-4b54-8018-1bed379e4029",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://hdinsight.kusto.windows.net').database('HDInsight').HBase_MemstoreReads",
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "Medium",
  "recommendationResourceType": "Microsoft.HDInsight/clusters",
  "recommendationFriendlyName": "HBaseMemstoreReadPercentage",
  "recommendationMetadataState": "Active",
  "owner": {
    "email": "hdistr@microsoft.com",
    "icm": {
      "routingId": "MDM://HDIStreaming",
      "service": "HDInsight",
      "team": "Streaming & Store (HBase, Phoenix, Kafka, Storm, OMS)"
    },
    "serviceTreeId": "2ee735d6-5f03-45c3-bf11-fc1dbb1aa135"
  },
  "ingestionClientIdentities": [],
  "version": 2.0,
  "learnMoreLink": "https://docs.microsoft.com/azure/hdinsight/hbase/apache-hbase-advisor",
  "description": "Reads happen on most recent data",
  "longDescription": "More than 75% of your read requests are landing on the memstore. That indicates that the reads are primarily on recent data. This suggests that even if a flush happens on the memstore, the recent file needs to be accessed and that file needs to be in the cache.",
  "potentialBenefits": "If the reads are on the most recent data, the suggested config changes will help you do the reads from the memory as much as possible, therefore helping with faster read performance.",
  "actions": [
    {
      "actionId": "2b83b49c-8c01-486b-a569-b22c8c6f2154",
      "description": "The given namespace/table/family has greater than 75% of reads happening on memstore",
      "actionType": "Document",
      "documentLink": "https://docs.microsoft.com/azure/hdinsight/hbase/apache-hbase-advisor#optimize-hbase-to-read-most-recently-written-data"
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "5c02943a-78e9-4e4c-8757-ed58bff6ac13",
      "actionType": "Blade",
      "extensionName": "HubsExtension",
      "bladeName": "ResourceMenuBlade",
      "metadata": {
        "id": "{resourceId}"
	  }
    }
  },
  "displayLabel": "HBase Query advisor for tuning memstore reads",
  "additionalColumns": [
  {
      "name": "nsName",
      "title": "NameSpaceName"
    },
	{
      "name": "tableName",
      "title": "TableName"
    },
    {
      "name": "familyName",
      "title": "FamilyName"
    }
  ],
  "tip": "HBase reads tuning",
  "costSavingInfo": "",
  "testData": "c36fd9e7-e5b1-4d3e-bb85-2e538040258b,/subscriptions/c36fd9e7-e5b1-4d3e-bb85-2e538040258b/resourceGroups/blr_hbase/providers/Microsoft.HDInsight/clusters/hbase-216-writes,\"{\"\"nsName\"\": \"\"default\"\",\"\"tableName\"\": \"\"T_T1_t2_T3\"\",\"\"familyName\"\": \"\"f1\"\",\"\"memstoreReadPercentage\"\": \"\"75.0\"\"}\""
}
---
