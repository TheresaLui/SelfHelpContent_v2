<properties
    pageTitle="HDInsight cluster in safemode"
    description="HDInsight cluster in safemode"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="nealbh"
    displayOrder="33"
    articleId="Hdi_Crud_Safemode"
    diagnosticScenario="HDInsightSafeModeInsight"
    selfHelpType="rca"
    supportTopicIds="32588504"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found the following issue

## Problem
The HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> is running in safemode causing storage access such as read/write operations to fail. 

## **Recommended steps**
* Log onto cluster

* Disable safemode
hdfs dfsadmin -D 'fs.default.name=hdfs://<!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName-->/' -safemode leave

## Further Reading
Please refer to this [blog post]](https://blogs.msdn.microsoft.com/bigdatasupport/2016/03/16/hdinsight-hdfs-can-stay-in-safe-mode-after-a-scale-down/) for more information regarding HDFS in safemode 