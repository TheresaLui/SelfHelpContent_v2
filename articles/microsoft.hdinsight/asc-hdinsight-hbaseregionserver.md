<properties
    pageTitle="HDInsight HBase Region Server Not Available"
    description="HDInsight HBase Region Server Not Available"
    infoBubbleText="HDInsight HBase cluster has some regions not available. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="shawnawei"
    ms.author="xunwei"
    displayOrder="156"
    articleId="Hdi_Health_HBaseRegionServer"
    diagnosticScenario="HDInsightHBaseRegionServerInsight"
    selfHelpType="rca"
    supportTopicIds="32636453, 32636449"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found the following issue

We determined that the HDInsight HBase cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> has regions not available.

## **Recommended Steps**

1. Stop HBase from Ambari portal.

2. Execute hadoop fs -ls -R /hbase/WALs/ > /tmp/wals.out to get fresh list of WALs.

3. Move the \*-splitting directories to a temporary folder, splitWAL, and delete the \*-splitting directories.

4. Execute hbase zkcli command to connect with zookeeper shell.

5. Execute rmr /hbase-unsecure/splitWAL.

6. Restart HBase service.

## **Recommended Documents**

* [Issues with region servers in Azure HDInsight](https://docs.microsoft.com/en-us/azure/hdinsight/hbase/hbase-troubleshoot-unassigned-regions#scenario-unassigned-regions%20%22)
