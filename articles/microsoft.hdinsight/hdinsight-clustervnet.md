<properties
    pageTitle="Azure HDInsight: Virtual Network"
    description="Azure HDInsight: Virtual Network"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="TobyTu"
    ms.author="jaserano, v-miegge"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32636507"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, mooncake"
    articleId="bfa4e56c-3fbc-461d-a7d5-1e485b42932b"
/>
# Azure HDInsight: Virtual Network

## Common HDInsight VNET issues

**I have created my cluster but forgot to add it to my VNet**

Unfortunately, there is no way to add a VNET to an existing cluster. You must [delete the existing cluster, then re-deploy a new cluster and add it to the VNET](https://docs.microsoft.com/azure/hdinsight/hdinsight-extend-hadoop-virtual-network#existingvnet).

**Forced tunneling to on-premise**

Forced tunneling is a user-defined routing configuration where all traffic from a subnet is forced to a specific network or location, such as an on-premises network. HDInsight does not support forced tunneling of traffic to on-premises networks.

**Ensure you have all the required IP addresses**

If you use either network security groups or user defined routes to control traffic, you must allow traffic from the IP addresses for Azure health and management services, so that they can communicate with your HDInsight cluster. Some IP addresses are region specific, and some addresses apply to all Azure regions. You may also need to allow traffic from the Azure DNS service if you aren't using a custom DNS. [Click here for the list of required IPs](https://docs.microsoft.com/azure/hdinsight/hdinsight-extend-hadoop-virtual-network#hdinsight-ip).

**Ensure you have the required ports open**

If you plan to use a firewall, and access the cluster from outside on certain ports, you might need to allow traffic on those ports needed for your scenario. [Click here for the list of ports for specific services](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-port-settings-for-services).

## **Recommended Documents**

* [Connectivity and Virtual Networks FAQ](https://docs.microsoft.com/en-au/azure/hdinsight/hdinsight-faq#connectivity-and-virtual-networks)
* [VNET and Networking](https://docs.microsoft.com/azure/hdinsight/hdinsight-extend-hadoop-virtual-network)
* [Connect HDInsight to your on-premises network](https://docs.microsoft.com/azure/hdinsight/connect-on-premises-network#configure-the-virtual-network-to-use-the-custom-dns-server)
