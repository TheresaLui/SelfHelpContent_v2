<properties
    pageTitle="Avere vFXT Networking Issues"
    description="Resolve issues with Avere vFXT networking."
    infoBubbleText="Avere vFXT Networking Issues"
    authors="jbut"
    ms.author="jebutl"
    displayOrder="1"
    articleId="averevfxt-networking"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32609693"
    resourceTags=""
    productPesIds="16506"
    cloudEnvironments="public, fairfax, usnat, ussec"
    ownershipId="StorageMediaEdge_AvereVFXT"
/>

# Avere vFXT Networking Issues

Please consider the following information when dealing with a network connectivity issue.

## *Debugging with Ping*

First, if this is a problem that involves clients accessing the Avere vFXT cluster, please re-categorize this issue under the "Client Access Issues" support topic.

All Avere vFXT nodes are pingable.  You may test network connectivity by running the *ping* command in order to determine if network interfaces are responding.  Sometimes it is helpful to debug a Linux VM in the VNet and subnet that contains the Avere vFXT cluster.  You may also benefit by testing connectivity from your on-premises network by sourcing *ping* packets from a machine on that network.

## *Resource Groups and Network Infrastructure*

This [Resource group and network infrastructure](https://docs.microsoft.com/azure/avere-vfxt/avere-vfxt-deploy-plan#resource-group-and-network-infrastructure) article describes that a resource group needs to be created for the Avere vFXT, but you can use existing VNets and subnets.

## *IP Address requirements*

Avere vFXT clusters require a number of IP addresses. [IP address requirements](https://docs.microsoft.com/azure/avere-vfxt/avere-vfxt-deploy-plan#ip-address-requirements) describes the different types of IP address ranges required to deplay an Avere vFXT cluster.

## *Cluster Access*

This [Cluster access](https://docs.microsoft.com/azure/avere-vfxt/avere-vfxt-deploy-plan#cluster-access) describes how to access the vFXT cluster.

## *DNS Configuration*

The Avere vFXT depends on round-robin DNS to provide load-balanced DNS access to clients. [Avere cluster DNS Configuration](https://docs.microsoft.com/azure/avere-vfxt/avere-vfxt-configure-dns) describes how to set this up.

## **Recommended Documents**

* [Troubleshooting connectivity problems between Azure VMs](https://docs.microsoft.com/azure/virtual-network/virtual-network-troubleshoot-connectivity-problem-between-vms)

