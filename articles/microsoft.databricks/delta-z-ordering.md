<properties 
    pageTitle="Diagnose and resolve issues with Delta Z-ordering" 
    description="Diagnose and resolve issues with Delta Z-ordering" 
    service="microsoft.databricks" 
    resource="workspaces" 
    authors="lahaddad" 
    ms.author="lahaddad" 
    displayOrder="15" 
    selfHelpType="generic" 
    supportTopicIds="32784343" 
    resourceTags="" 
    productPesIds="16432" 
    cloudEnvironments="public, fairfax, usnat, ussec" 
    articleId="f625afcc-4987-48f1-ac9d-934e84a8da1b" 
    ownershipId="AzureData_AzureDatabricks" 
/> 


# Diagnose and resolve issues with Delta Z-ordering 

## **Recommended Steps**

* **AnalysisException: Z-Ordering on [col1, col2] will be ineffective, because we currently do not collect stats for these columns.**

  By default, Delta Lake on Databricks collects statistics on the first 32 columns defined in your table schema. So if these columns are not in those first 32 columns, then stats will not be collected for them. To resolve the issue:

  * Reorder the columns in the table, so that these `n` columns will come to the first few columns in the table. You can issue an alter table statement to reorder the columns, so that you can bring these columns to the front of the table. Sample syntax: 
  
    ```
    ALTER TABLE table_name CHANGE [COLUMN] col_name col_name data_type [COMMENT col_comment] [FIRST|AFTER colA_name]
    ```
    
  * This requires rewriting the table data, because the stats are collected only at the time of writing data. Alternatively, you can recompute the stats by running the following commands:

     ```
     %scala 
     import com.databricks.sql.transaction.tahoe._ 
     import org.apache.spark.sql.catalyst.TableIdentifier 
     import com.databricks.sql.transaction.tahoe.stats.StatisticsCollection
     val tableName = "table_name" 
     val deltaLog = DeltaLog.forTable(spark, TableIdentifier(tableName)) 
     StatisticsCollection.recompute(spark, deltaLog)
     ```

## **Recommended Documents** 

* [Azure Databricks Platform release notes](https://docs.microsoft.com/azure/databricks/release-notes/product/) cover the features that we develop for the Azure Databricks platform 
* [Databricks Runtime release notes](https://docs.microsoft.com/azure/databricks/release-notes/runtime/) cover the features that we develop for Databricks cluster runtimes or images. This includes proprietary features and optimizations. 
* [Delta FAQs](https://docs.microsoft.com/azure/databricks/delta/delta-faq) 
* [Delta How-to](https://docs.microsoft.com/azure/databricks/delta/delta-intro) 
* [Resources](https://docs.microsoft.com/azure/databricks/delta/delta-resources) 
* [Best Practices](https://docs.microsoft.com/azure/databricks/delta/best-practices) 
* [Delta Lake Tips and Troubleshooting](https://docs.microsoft.com/azure/databricks/kb/delta/) 
* [Introductory Notebooks](https://docs.microsoft.com/azure/databricks/delta/intro-notebooks) 
