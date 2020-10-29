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
    cloudEnvironments="public, mooncake, Fairfax, usnat, ussec"
    articleId="bfa4e56c-3fbc-461d-a7d5-1e485b42932b"
	ownershipId="AzureData_HDInsight"
/>
# Azure HDInsight: Virtual Network

**Common HDInsight VNET issues**

**I have created my cluster but forgot to add it to my VNet**

There is no way to add a VNET to an existing cluster. You must [delete the existing cluster, then re-deploy a new cluster and add it to the VNET](https://docs.microsoft.com/azure/hdinsight/hdinsight-extend-hadoop-virtual-network#existingvnet).

**Forced tunneling to on-premise**

Forced tunneling is a user-defined routing configuration where all traffic from a subnet is forced to a specific network or location, such as an on-premises network. HDInsight does not support forced tunneling of traffic to on-premises networks.

**Ensure that you have all the required IP addresses**

If you use either network security groups or user defined routes to control traffic, you must allow traffic from the IP addresses for Azure health and management services, so that they can communicate with your HDInsight cluster. Some IP addresses are region-specific, and some addresses apply to all Azure regions. You may also need to allow traffic from the Azure DNS service if you aren't using a custom DNS. [Click here for the list of required IPs](https://docs.microsoft.com/azure/hdinsight/hdinsight-extend-hadoop-virtual-network#hdinsight-ip).

**Ensure that you have the required ports open**

If you plan to use a firewall and to access the cluster from outside on certain ports, you might need to allow traffic on those ports needed for your scenario. See [the list of ports for specific services](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-port-settings-for-services).

**Error: HiveMetastoreSchemaInitializationFailedErrorCode**

If you are using a custom Hive metastore, run `Hive Schema Tool` against your metastore to check for possible issues with metastore configuration. Also check if Azure services or subnet is whitelisted in the SQL Server firewall.

**Error: Unable to connect to cluster management endpoint** 

Ensure that the IPs in the [Health and management services: All regions](https://docs.microsoft.com/azure/hdinsight/hdinsight-management-ip-addresses#health-and-management-services-all-regions) document have been whitelisted. To verify that the configurations work, you can ping or [tracert](https://docs.microsoft.com/windows-server/administration/windows-commands/tracert) to the required IP addresses from an Azure Virtual Machine in the custom VNet to test whether the IP addresses are accessible from the virtual machines. If you are unable to access these IPs, it validates that your configured firewall is not allowing connections to the whitelisted IPs.

**Error: Unable to connect to cluster**

Possible solution: If you are using user-defined routes (UDRs), specify a route and allow outbound traffic from the VNET to the above IPs with the next hop set to **Internet**.

For more information, see the following links:
* [HDInsight Controlling network traffic](https://docs.microsoft.com/azure/hdinsight/hdinsight-plan-virtual-network-deployment#networktraffic)
* [HDInsight management IP addresses](https://docs.microsoft.com/azure/hdinsight/hdinsight-management-ip-addresses)

## **Recommended Documents**

* [Connectivity and Virtual Networks FAQ](https://docs.microsoft.com/en-au/azure/hdinsight/hdinsight-faq#connectivity-and-virtual-networks)
* [VNET and Networking](https://docs.microsoft.com/azure/hdinsight/hdinsight-extend-hadoop-virtual-network)
* [Connect HDInsight to your on-premises network](https://docs.microsoft.com/azure/hdinsight/connect-on-premises-network#configure-the-virtual-network-to-use-the-custom-dns-server)
* [Create Cluster Error Dictionary](https://docs.microsoft.com/azure/hdinsight/create-cluster-error-dictionary)
* [Azure Security Baseline for HDInsight](https://docs.microsoft.com/azure/hdinsight/security-baseline)
