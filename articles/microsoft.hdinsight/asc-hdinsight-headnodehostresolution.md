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
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> not all nodes are pointing to the same headnodehost
<!--issueDescription-->
Nodes within your HDInsight cluster are experiencing a problem due to some nodes not pointing to the same headnodehost. 
<!--/issueDescription-->

## **Recommended Steps**

* SSH onto the nodes, given from Support Engineer, within the HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName-->
* Open the hosts files vi /etc/hosts
* Update the host files with the headnodehost pointing to the other headnode
* Save and close the file
