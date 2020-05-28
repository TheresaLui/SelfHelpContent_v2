<properties
    pageTitle="Azure HDInsights: HBase Service Unhealthy"
    description="Azure HDInsights: HBase Service Unhealthy"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="genlin"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32636453"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="f18d50b6-ccf5-407b-9b49-3c59bfa0eaec"
	ownershipId="AzureData_HDInsight"
/>
# Restart operation on HBase

## **Recommended Documents**

* [Restart operation on HBase Region Server fails to complete](https://hdinsight.github.io/hbase/hbase-regionserver-restart-failed)
* Region server hotspotting can occur when writing records with sequential keys to HBase. Please read [here](https://docs.microsoft.com/azure/hdinsight/hdinsight-phoenix-in-hdinsight#salted-tables) to learn about mitigations.
* HBase Master (HMaster) can fail with errors such as "Atomic renaming failure" or "No server address listed in hbase". To resolve these issues, check the following the recommended documents:

     * [HBase Master not starting up](https://hdinsight.github.io/hbase/hbase-master-not-starting-up)
     * [Ambari agent heartbeat lost Alert](https://hdinsight.github.io/ambari/ambari-agent-heartbeat-lost.html)
