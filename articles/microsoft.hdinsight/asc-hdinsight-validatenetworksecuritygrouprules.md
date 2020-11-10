<properties
    pageTitle="HDInsight Invalid Network Security Group Rules"
    description="HDInsightValidateNetworkSecurityGroupRules"
    infoBubbleText="Found recent invalid network security group rules error. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="anirudhrege"
    ms.author="v-anreg"
    displayOrder=""
    articleId="Hdi_Crud_InvalidNetworkSecurityGroupRules"
    diagnosticScenario="HDInsightValidateNetworkSecurityGroupRulesInsight"
    selfHelpType="rca"
    supportTopicIds="32636423, 32636507"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
There is a problem with the inbound network security group rules configured for your HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName-->.
<!--/issueDescription-->

## **Recommended Steps**

* Go to the Azure Portal and identify the NSG that is associated with the subnet where the cluster is being deployed
* In the "Inbound security rules" section, make sure the rules allow inbound access to port 443 for the IP addresses <!--$MissingIp-->[MissingIp]<!--/$MissingIp-->

## **Recommended Documents**

* [HDInsight with network security groups and user-defined routes](https://docs.microsoft.com/azure/hdinsight/hdinsight-extend-hadoop-virtual-network#hdinsight-ip)
 
