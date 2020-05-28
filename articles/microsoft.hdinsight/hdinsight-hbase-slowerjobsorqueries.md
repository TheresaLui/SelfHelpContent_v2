<properties
    pageTitle="HBase: Slow queries or jobs"
    description="TSG / How-to for know scenario"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="ramakoni1"
    ms.author="deeptivu"
    displayOrder="99"
    selfHelpType="resource"
    supportTopicIds="32636451"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="hdinsight-slowerjobsorqueries"
	ownershipId="AzureData_HDInsight"
/>
# Slow HBase queries or jobs

## **Recommended Steps**

* Follow the performance tuning suggestions in [Troubleshoot Apache HBase performance issues on Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/hbase/troubleshoot-hbase-performance-issues#server-side-config-tunings) to get optimal performance for your HBase queries
* Implement accelerated writes to get 4 to 10-times faster writes. Accelerated writes uses Azure premium SSD managed disks to improve performance of the Apache HBase Write Ahead Log (WAL). For more information, see [Azure HDInsight Accelerated Writes for Apache HBase](https://docs.microsoft.com/azure/hdinsight/hbase/apache-hbase-accelerated-writes).
* Use a [Premium Block Blob Storage Account](https://azure.microsoft.com/blog/azure-premium-block-blob-storage-is-now-generally-available) as your remote storage to gain significant improvements in read operations. This option is available only if the Write Ahead Logs feature is enabled.

### Troubleshooting specific scenarios

* If you are using the hbase hbck command and get timeout errors, see [Timeouts with 'hbase hbck' command in Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/hbase/hbase-troubleshoot-timeouts-hbase-hbck)
* If your restart operation fails, see [Restart operation on HBase Region Server fails to complete](https://hdinsight.github.io/hbase/hbase-regionserver-restart-failed.html)
