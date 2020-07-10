<properties
    pageTitle="HDInsight failure due to full subnet"
    description="HDInsight failure due to full subnet"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="anirudhrege"
    ms.author="v-anreg"
    displayOrder="28"
    articleId="Hdi_fullsubnet"
    diagnosticScenario="HDInsightSubnetIsFullInsight"
    selfHelpType="rca"
    supportTopicIds="32636423, 32681537"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found the following issue

## Problem
<!--issueDescription-->
Deployment of the HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> failed within subscription <!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId--> because the subnet does not have sufficient free IP addresses to match the number of nodes of the cluster.
<!--/issueDescription-->

## **Recommended Steps**

In order to create space on the virtual network please do **one** of the three steps below:

* Delete unused resources within the subnet opening up IP addresses that can be utilized for the cluster scaling
* [Add a subnet](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-subnet#add-a-subnet) and create a new HDInsight cluster within the newly created subnet
* [Change subnet settings](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-subnet#change-subnet-settings) to the existing virtual network to include a larger address space

## Subnets at Capacity
<!--$Subnet-->[Subnet]<!--/$Subnet-->
