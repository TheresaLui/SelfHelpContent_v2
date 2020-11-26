<properties
    pageTitle="Update statistics on table columns"
    description="Update statistics on table columns"
    authors="aadevteam"
    ms.author="aadevteam"
    articleId="01dea77b-3ca4-4583-9b09-88f5a8fd5857_USSec"
    selfHelpType="advisorRecommendationMetadata"
    cloudEnvironments="USSec"
    ownershipId="AzureData_SynapseAnalytics"
/>
# Update statistics on table columns
---
{
  "recommendationOfferingId": "36bdbad1-7a98-45b6-bba9-5de8c197f991",
  "recommendationOfferingName": "Azure Synapse Analytics",
  "$schema": "AdvisorRecommendation",
  "recommendationTypeId": "01dea77b-3ca4-4583-9b09-88f5a8fd5857",
  "dataSourceMetadata": {
    "streamNamespace": "cluster('https://sqlazureussece.kusto.core.microsoft.scloud').database('sqlazure1').dw_advisor_UpdateTableStatistics",
    "schemaVersion": 2.0,
    "dataSource": "Kusto",
    "refreshInterval": "12:00:00"
  },
  "recommendationCategory": "Performance",
  "recommendationImpact": "High",
  "recommendationResourceType": "Microsoft.Sql/sqlDataWarehouses",
  "recommendationFriendlyName": "UpdateTableStatisticsSqlDW",
  "recommendationMetadataState": "Active",
  "portalFeatures": [],
  "owner": {
    "email": "sqldwninjas@service.microsoft.com",
    "icm": {
      "routingId": "AIMS://AZURESQLDB/DATAWAREHOUSE/ADVISORS",
      "service": "Azure SQL DB",
      "team": "Datawarehouse"
    },
    "serviceTreeId": "6d302332-f404-4848-9509-b8a6b81510f7"
  },
  "recommendationTimeToLive": 86400,
  "version": 2.0,
  "learnMoreLink": "https://aka.ms/learnmorestatistics",
  "description": "Update statistics on table columns",
  "longDescription": "We have detected that you do not have up-to-date table statistics which may be impacting query performance. The query optimizer uses up-to-date statistics to estimate the cardinality or number of rows in the query result which enables the query optimizer to create a high quality query plan.",
  "potentialBenefits": "Increase query performance",
  "actions": [
    {
      "actionId": "ead27582-9549-42f3-881d-c21c2d3b2a12",
      "description": "Update table statistics",
      "actionType": "Document",
      "documentLink": "https://aka.ms/actionsupdatestatistics"
    },
    {
      "actionId": "4a3d2be3-bc2c-4b7c-a97f-2de8d4e4cfad",
      "description": "View impacted tables",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "QueryEditorBlade",
      "metadata": {
        "resourceId": "{resourceId}",
        "queryText": "-- data skew -> cmp_rows>1mil, skew >= 10%\n-- missing stats -> cmp_rows>1mil, ctl_rows=1000\n-- outdated stats -> cmp_rows>1mil, cmp_rows <> ctl_rows (for (cmp_rows-ctl_rows) > 20%)\n\ndeclare @minRows int=1000000;\ndeclare @minSkewPercent decimal=10.0;\ndeclare @missingStatCtlRowCount int=1000;\ndeclare @CtlCmpRowDifferencePercentageForOutdatedStats decimal=20.0;\n\nwith cmp_details as\n(\n       select tm.object_id, ps.index_id, ps.distribution_id, count(ps.partition_number) [partitions], sum(ps.row_count) cmp_row_count\n       from sys.dm_pdw_nodes_db_partition_stats ps\n              join sys.pdw_nodes_tables nt on nt.object_id=ps.object_id and ps.distribution_id=nt.distribution_id\n              join sys.pdw_table_mappings tm on tm.physical_name=nt.name\n       where ps.index_id<2\n       group by tm.object_id, ps.index_id, ps.distribution_id\n)\n, cmp_summary as\n(\n       select object_id, index_id, sum(cmp_row_count) cmp_row_count\n              , (max(cmp_row_count)-min(cmp_row_count)) highest_skew_rows_difference\n              , convert(decimal(10,2),((max(cmp_row_count) - min(cmp_row_count))*100.0 / nullif(sum(cmp_row_count),0))) skew_percent\n       from cmp_details\n       group by object_id, index_id\n)\n, ctl_summary as\n(\n       select t.object_id, i.index_id, s.name sch_name, t.name table_name, i.type_desc table_type, dp.distribution_policy_desc distribution_type, count(p.partition_number) [partitions], sum(p.rows) ctl_row_count\n       from sys.schemas s\n              join sys.tables t on t.schema_id=s.schema_id\n              join sys.pdw_table_distribution_properties dp on dp.object_id=t.object_id\n              join sys.indexes i on i.object_id=t.object_id and i.index_id<2\n              join sys.partitions p on p.object_id=t.object_id and p.index_id=i.index_id\n       group by t.object_id, i.index_id, s.name, t.name, i.type_desc, dp.distribution_policy_desc\n)\n, [all_results] as\n(\n       select ctl.object_id, ctl.index_id, ctl.sch_name, ctl.table_name, ctl.table_type, ctl.distribution_type, ctl.[partitions]\n              , ctl.ctl_row_count, cmp.cmp_row_count, convert(decimal(10,2),(abs(ctl.ctl_row_count - cmp.cmp_row_count)*100.0 / nullif(cmp.cmp_row_count,0))) ctl_cmp_difference_percent\n              , cmp.highest_skew_rows_difference, cmp.skew_percent\n              , case \n                     when (ctl.ctl_row_count = @missingStatCtlRowCount) then 'missing stats'\n                     when ((ctl.ctl_row_count <> cmp.cmp_row_count) and ((abs(ctl.ctl_row_count - cmp.cmp_row_count)*100.0 / nullif(cmp.cmp_row_count,0)) > @CtlCmpRowDifferencePercentageForOutdatedStats)) then 'outdated stats'\n                     else null\n                end stat_info\n              , case when (cmp.skew_percent >= @minSkewPercent) then 'data skew' else null end skew_info\n       from ctl_summary ctl\n              join cmp_summary cmp on ctl.object_id=cmp.object_id and ctl.index_id=cmp.index_id\n)\nselect *\nfrom [all_results]\nwhere cmp_row_count>@minRows and (stat_info is not null or skew_info is not null)\norder by sch_name, table_name"
      }
    }
  ],
  "resourceMetadata": {
    "action": {
      "actionId": "06687182-7041-4cb3-a13c-30c5b6754dcf",
      "actionType": "Blade",
      "extensionName": "SqlAzureExtension",
      "bladeName": "DataWarehouseBlade",
      "metadata": {
        "id": "{resourceId}"
      }
    }
  },
  "displayLabel": "Update table statistics",
  "additionalColumns": [
    {
      "name": "impactedTableCount",
      "title": "Total Impacted Tables"
    }
  ]
}
---
