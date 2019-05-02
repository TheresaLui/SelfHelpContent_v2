<properties
    pageTitle="HDInsight cluster nodes are pointing to different headnodehosts"
    description="HDInsight cluster nodes are pointing to different headnodehosts"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="nealbh"
    ms.author="nebhatta"
    displayOrder="122"
    articleId="Hdi_Health_HeadNodeHost"
    diagnosticScenario="HDInsightHeadnodehostInsight"
    selfHelpType="rca"
    supportTopicIds="32636430"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> not all nodes are pointing to the same headnodehost

The following nodes <!--$headnodehosts-->[headnodehosts]<!--/$headnodehosts--> within your HDInsight cluster is currently suffering from not all nodes pointing to the same headnodehost. 

## **Recommended Steps**

* SSH onto the nodes listed above within the HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName-->
* Open the hosts files vi /etc/hosts
* Update the host files with the headnodehost pointing to the other headnode
* Save and close the file