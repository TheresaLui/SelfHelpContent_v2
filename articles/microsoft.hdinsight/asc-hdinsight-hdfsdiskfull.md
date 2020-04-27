<properties
    pageTitle="HDInsight Hdfds Disk is running out of space"
    description="HDInsight Insight to check if Hdfs Disk is runnig out of space"
    infoBubbleText="Found error with Hdfs Disk space in cluster. See details on the right"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="Sainath"
    ms.author="v-samaly"
    displayOrder=""
    articleId="HDI_HDFSDiskFull"
    diagnosticScenario="HDInsightHdfsDiskFullInsight"
    selfHelpType="rca"
    supportTopicIds="32636429,32636432"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, mooncake, blackforest, fairfax, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found the following issue

<!--issueDescription-->
HDFS is running out of space for the following host(s): <!--$Hosts-->[Hosts]<!--/$Hosts--> in the cluster
<!--/issueDescription-->
	

## **Recommended Steps**

Please follow the steps given in the document:

* [HDFS gets full in Azure HDInsight with many Hive temporary files](https://blogs.msdn.microsoft.com/bigdatasupport/2016/08/15/hdfs-gets-full-in-azure-hdinsight-with-many-hive-temporary-files/)
