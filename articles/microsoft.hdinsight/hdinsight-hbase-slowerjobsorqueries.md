<properties
    pageTitle="HBase: Slow queries or jobs"
    description="TSG / How-to for know scenario"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="ramakoni1"
    ms.author="deeptivu"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32636451"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
    articleId="hdinsight-slowerjobsorqueries"
/>
# Slow HBase queries or jobs

## **Recommended Documents**

* [Server-side configuration tuning](https://docs.microsoft.com/azure/hdinsight/hbase/troubleshoot-hbase-performance-issues#server-side-config-tunings) to improve performance

* Did you know that Writes to Hbase would be 4 to 10x faster with our Accelerated Writes feature for Apache HBase in Azure HDInsight? Accelerated Writes uses Azure premium SSD managed disks to improve performance of the Apache HBase Write Ahead Log (WAL). To learn more about it please follow [Azure HDInsight Accelerated Writes for Apache HBase](https://docs.microsoft.com/azure/hdinsight/hbase/apache-hbase-accelerated-writes)

* Use [Premium Block Blob Storage Account](https://azure.microsoft.com/blog/azure-premium-block-blob-storage-is-now-generally-available) as your remote storage to gain significant improvement in read operations. This option is possible only if Write Ahead Logs feature is enabled.

* [Troubleshoot Apache HBase performance issues on Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/hbase/troubleshoot-hbase-performance-issues#server-side-config-tunings)

### Troubleshooting specific scenario

* [Timeouts with 'hbase hbck' command in Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/hbase/hbase-troubleshoot-timeouts-hbase-hbck)
* [Restart operation on HBase Region Server fails to complete](https://hdinsight.github.io/hbase/hbase-regionserver-restart-failed.html)
