<properties
	pageTitle="Z-Ordering Delta table throws Analysis Exception because of not collecting stats for columns"
	description="Z-Ordering Delta table throws Analysis Exception because of not collecting stats for columns"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="e464a9ea-4e13-4081-94d1-322904c156f2"
   	ownershipId="AzureData_AzureDatabricks"
/>

# Z-Ordering Delta table throws Analysis Exception because of not collecting stats for columns

<!--issueDescription-->

Based on provided details and initial investigation, please find a summary of issue as below:

## **Problem**

While trying to Z-order Delta table, receiving below error:
AnalysisException: "Z-Ordering on [col1, col2] will be ineffective, because we currently do not collect stats for these columns. 

## **Cause**

This error message is basically telling us that Z-ordering on columns will not be effective, as we currently do not collect stats on these. By default, Delta Lake on Databricks collects statistics on the first 32 columns defined in your table schema. So if these columns are not in those first 32 columns, then by default stats will not be collected for them.

## **Solution**

Re-order the columns in the table, so that these  columns will come to the first few columns in the table. You can issue an alter table statement to re-order the columns, so that you can bring these columns to the front of the table. 

Here is the sample syntax:

    ALTER TABLE table_name CHANGE [COLUMN] col_name col_name data_type [COMMENT col_comment] [FIRST|AFTER colA_name]

For example,  below statement will bring the col-name to the first column in the table:

    %sql 
    ALTER TABLE delta-table-name CHANGE COLUMN col-name col-name data-type FIRST

This requires re-writing the table data, as the stats are collected only at the time of writing data. Alternatively, you can re-compute the stats by using below commands:

    %scala 
    import com.databricks.sql.transaction.tahoe._ 
    import org.apache.spark.sql.catalyst.TableIdentifier 
    import com.databricks.sql.transaction.tahoe.stats.StatisticsCollection
    val tableName = "<table_name>" 
    val deltaLog = DeltaLog.forTable(spark, TableIdentifier(tableName)) 
    StatisticsCollection.recompute(spark, deltaLog)

## **Recommended Documents**

* [Z-Ordering](https://docs.microsoft.com/azure/databricks/delta/optimizations/file-mgmt#--z-ordering-multi-dimensional-clustering)
* [Data Skipping](https://docs.microsoft.com/azure/databricks/delta/optimizations/file-mgmt#--data-skipping)

<!--/issueDescription-->