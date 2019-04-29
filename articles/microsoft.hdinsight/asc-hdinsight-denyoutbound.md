<properties
    pageTitle="HDInsight cluster contains deny outbound rule within Network Security Group"
    description="HDInsight cluster contains deny outbound rule within Network Security Group"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="nealbh"
    ms.author="nebhatta"
    displayOrder="88"
    articleId="Hdi_Network_DenyOutbound"
    diagnosticScenario="HDInsightInsufficientNumberOfCoresInsight"
    selfHelpType="rca"
    supportTopicIds="32629159, 32636423, 32636422"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found the following issue

We determined that the network security gorup associated with the HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> have the following network security group rules that would deny outbound access from the cluster. <!--$Details-->[Details]<!--/$Details-->

## **Recommended Steps**

* Restricting outbound access is not supported, please remove or update the following rules to allow outbound access from the HDInsight cluster.

## **Recommended Documents** 

* [Controlling network traffic](https://docs.microsoft.com/en-us/azure/hdinsight/hdinsight-extend-hadoop-virtual-network#networktraffic)
