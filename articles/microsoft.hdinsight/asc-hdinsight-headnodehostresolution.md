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

1. SSH onto the nodes, provided by your Support Engineer, within the HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName-->
2. Open the hosts files **vi /etc/hosts**
3. Update to make sure all nodes in the cluster have **/etc/hosts** files, and point to the same and correct headnodehost VM. Look for keyword 'headnodehost' in a line in **/etc/hosts** file, for example: <br>

   `10.0.0.16       hn1-spec1k.i2ypcarpryeebf2lwa3xcs1gaa.jx.internal.cloudapp.net  hn1-spec1k      headnodehost    hn1-spec1k.i2ypcarpryeebf2lwa3xcs1gaa.jx.internal.cloudapp.net.  headnodehost.   # SlaveNodeManager`

4. Save and close the file
