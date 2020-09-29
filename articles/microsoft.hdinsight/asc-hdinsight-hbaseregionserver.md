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
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
We determined that the HDInsight HBase cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> has regions unavailable. Region offline could be due to multiple reasons. Potential cause here could be several regions are "in transition" for a long time, as can be seen from HMaster UI and are actually offline. Due to sheer number of regions that are attempting to transition, HMaster times out and is unable to bring online these offline regions. 
<!--/issueDescription-->

## **Recommended Steps**

1. First, attempt to fix by running `hbase hbck -fixAssignments -ignorePreCheckPermission`
2. *(BETA)* Following script is developed to fix the issue and verify the fix. Please attempt this method first, before trying next steps or calling SME: 
    
    * If you have ssh access to the cluster, download this script with `sudo wget: https://raw.githubusercontent.com/Azure/hbase-utils/master/scripts/clearregionintransitionznode.sh `
    * Execute the script with `sudo bash clearregionintransitionznode.sh`
    * Feedback on the experience and possible enhancements would be appreciated

3. Following below steps if above fails:

    - Run `hbase zkcli`
    - `rmr /hbase/regions-in-transition` (or `rmr /hbase-unsecure/regions-in-transition`)
    - Exit `hbase zkcli`
    - Restart Active HMaster from Ambari
    - Run `hbase hbck` again to check issue is fixed
    
