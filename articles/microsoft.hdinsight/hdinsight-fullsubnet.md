<properties
    pageTitle="HDInsight failure due to full subnet"
    description="HDInsight failure due to full subnet"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="nealbh"
    displayOrder="28"
    articleId="Hdi_fullsubnet"
    diagnosticScenario="HDInsightSubnetFullInsight"
    selfHelpType="rca"
    supportTopicIds="32511166, 32588504"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

## Problem

Scaling of the HDInsight cluster failed within subscription <!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId--> because the subnet in which this HDInsight cluster is deployed does not have sufficient free IP addresses to match the number of nodes you would like to scale up the cluster.

## **Recommended steps**
In order to create space on the virtual network please do **one** of the three steps below:

* Delete un-used resources within the subnet opening up IP addresses that can be utilized for the cluster scaling.

* [Add a subnet](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-subnet#add-a-subnet) and create a new HDInsight cluster within the newly created subnet.

* [Change subnet settings](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-subnet#change-subnet-settings) to the existing virtual network to include a larger address space.

## Subnets at capacity
<!--$Subnet-->[Subnet]<!--/$Subnet-->