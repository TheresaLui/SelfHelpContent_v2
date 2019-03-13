<properties
    pageTitle="HDInsight Ambari Metrics Collector malfunction"
    description="Ambari Metrics Collector is not recieving metrics"
    infoBubbleText="Found recent Ambari Metrics Collector error. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="nealbh"
    ms.author="nebhatta"
    displayOrder=""
    articleId="Hdi_AmbariMetricsCollector"
    diagnosticScenario="HDInsightAmbariMetricsCollectorInsight"
    selfHelpType="rca"
    supportTopicIds="32629007, 32629006, 32629024"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found the following issue

There is a problem with the Ambari Metrics Collector configured for your HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName-->.

## **Recommended Steps**

### Login into the Ambari portal

1.  Set AMS to maintenance 
2.  Stop AMS from Ambari  
3.  Identify the following from the **AMS Configs** screen:

    1.  `hbase.rootdir` (Default value is `file:///mnt/data/ambari-metrics-collector/hbase`)  
    2.  `hbase.tmp.dir`(Default value is `/var/lib/ambari-metrics-collector/hbase-tmp`)  

### SSH into headnode0. as superuser

1. Remove the AMS zookeeper data by backing up and removing the contents of  `'hbase.tmp.dir'/zookeeper`
2. Remove any Phoenix spool files from `'hbase.tmp.dir'/phoenix-spool` folder 
3. **Note**: It is worthwhile to skip this step and first restarting AMS to see if the issue is resolved. If AMS is still failing to come up, try this step: AMS data would be stored in `hbase.rootdir` identified above. Use regular OS commands to backup and remove the files: ` # tar czf /mnt/backupof-ambari-metrics-collector-hbase-$(date +%Y%m%d-%H%M%S).tar.gz /mnt/data/ambari-metrics-collector/hbase`  

### Restart AMS using Ambari

## **Recommended Documents**

* [Cleaning up Ambari Metrics System Data](https://cwiki.apache.org/confluence/display/AMBARI/Cleaning+up+Ambari+Metrics+System+Data+-+2.4.0)
