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

Scaling of the HDInsight cluster failed within subscription <!--$SubscriptionId-->SubscriptionId<!--/$SubscriptionId--> because of subnet being full.

## **Recommended steps**
In order to create space on the virtual network please do **one** of the two steps below:

1. [Add a subnet](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-manage-subnet#add-a-subnet) to the existing virtual network

1. [Change subnet settings](https://docs.microsoft.com/en-us/azure/virtual-network/virtual-network-manage-subnet#change-subnet-settings) to the existing virtual network.

## Subnets at capacity
<!--$Subnet-->[Subnet]<!--/$Subnet-->