<properties
    pageTitle="Scale HDInsight Cluster"
    description="TSG / How-to for know scenario"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="jaserano, v-miegge"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32636492"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
    articleId="hdinsight-scale-cluster"
/>

# Scale HDInsight Cluster

## Common HDInsight VNET issues

### I have created my cluster, but forgot to add it to my VNet

Unfortunately, there is no way to add a VNET to an existing cluster. You must delete the existing cluster, then re-deploy a new cluster and add it to the VNET. [See link here for more information](https://docs.microsoft.com/azure/hdinsight/hdinsight-extend-hadoop-virtual-network#existingvnet).

### Forced tunneling to on-premise

Forced tunneling is a user-defined routing configuration where all traffic from a subnet is forced to a specific network or location, such as an on-premises network. HDInsight does not support forced tunneling of traffic to on-premises networks.

### Please ensure you have all the required IP addresses

If you use either network security groups or user defined routes to control traffic, you must allow traffic from the IP addresses for Azure health and management services, so that they can communicate with your HDInsight cluster. Some IP addresses are region specific, and some addresses apply to all Azure regions. You may also need to allow traffic from the Azure DNS service if you aren't using a custom DNS. [Click here for the list of required IPs](https://docs.microsoft.com/azure/hdinsight/hdinsight-extend-hadoop-virtual-network#hdinsight-ip).

### Please ensure you have the required ports open

If you plan to use a firewall, and access the cluster from outside on certain ports, you might need to allow traffic on those ports needed for your scenario. [Click here for the list of ports for specific services](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-port-settings-for-services).

## **Recommended Documents**

* [Scale HDInsight clusters ](https://docs.microsoft.com/azure/hdinsight/hdinsight-scaling-best-practices)<br>
* [Automatically scale Azure HDInsight clusters (preview)](https://docs.microsoft.com/azure/hdinsight/hdinsight-autoscale-clusters?toc=%2F%2Fazure%2Fhdinsight%2Fhadoop%2FTOC.json&bc=%2F%2Fazure%2Fbread%2Ftoc.json) 
