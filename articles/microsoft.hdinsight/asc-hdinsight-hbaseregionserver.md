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
<!--issueDescription-->
We determined that the HDInsight HBase cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> has regions not available. Region offline could be due to multiple reasons. Potential cause here could be several regions are "in transition" for a long time, as can be seen from HMaster UI and are actually offline. Due to sheer number of regions that are attempting to transition HMaster times out and is unable to online these offline regions. 
<!--/issueDescription-->

## **Recommended Steps**
1. First, attempt to fix by running hbase hbck -fixAssignments -ignorePreCheckPermission, if this doesn't work look below.

2. (BETA) Following script is developed to fix the issue and verify the fix. Please attempt this method first, before trying next steps or calling SME. Feedback on the experience and possible enhancements would be appreciated.
    - If you have ssh access to the cluster, please download this script via sudo wget: https://raw.githubusercontent.com/Azure/hbase-utils/master/scripts/clearregionintransitionznode.sh 
    - Execute script as sudo bash clearregionintransitionznode.sh

3. Following below steps if above fails:
    - Run hbase zkcli
    - rmr /hbase/regions-in-transition (or rmr /hbase-unsecure/regions-in-transition)
    - Exit hbase zkcli
    - Restart Active HMaster from Ambari
    - Run hbase hbck again to check issue is fixed

## **Recommended Documents**

* [Issues with region servers in Azure HDInsight](https://msdata.visualstudio.com/HDInsight/_wiki/wikis/HDInsight.wiki?pagePath=%2FWIKI%2FEngineering%2FHBase%20troubleshoot&pageId=1248&wikiVersion=GBwikiMaster&anchor=region-server-related-issues)
