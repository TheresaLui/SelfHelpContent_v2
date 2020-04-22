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
    diagnosticScenario="HDInsightDenyOutboundInsight"
    selfHelpType="rca"
    supportTopicIds="32636423, 32636507"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>
# HDInsight cluster contains deny outbound rule within Network Security Group

## We ran diagnostics on your resource and found the following issue

<!--issueDescription-->
We determined that the network security group associated with the HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> have the following network security group rules that would deny outbound access from the cluster. 

<!--$Details-->[Details]<!--/$Details-->
<!--/issueDescription-->

## **Recommended Steps**

* Restricting outbound access is not supported. Please remove or update the following rules to allow outbound access from the HDInsight cluster.
* [Configure outbound network traffic for Azure HDInsight clusters using Firewall](https://docs.microsoft.com/azure/hdinsight/hdinsight-restrict-outbound-traffic)

## **Recommended Documents** 

* [Controlling network traffic](https://docs.microsoft.com/azure/hdinsight/hdinsight-extend-hadoop-virtual-network#networktraffic)
