<properties
    pageTitle="Common Customization Issues"
    description="Cluster Creation Fails Due To an Issue With Custom DNS Setup"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="v-miegge"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32636488"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, MoonCake, Fairfax, usnat, ussec"
    articleId="6a60e737-a15c-44df-8320-273b54797713"
	ownershipId="AzureData_HDInsight"
/>
# Common Customization Issues

## **Recommended Steps**

**Custom Script Actions**

Microsoft support teams can only address issues that occur when loading the script. Any errors during the execution of custom scripts is outside the scope of a support ticket. Please use our forums or other channels for troubleshooting errors which occur during the execution of custom scripts.

[Custom Script Actions Troubleshooting](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-customize-cluster-linux#troubleshooting)

**Adding an additional service to an existing cluster**

Microsoft can only support additional applications that are part the cluster creation process. For any additional applications/services outside of the cluster creation process, please contact that application/service provider for support.

For a list of supported components, see [What are the Apache Hadoop components and versions available with HDInsight?](https://docs.microsoft.com/azure/hdinsight/hdinsight-component-versioning#apache-hadoop-components-available-with-different-hdinsight-versions)

**Note**: Support for individual components can also vary by cluster type. For example, Spark is not supported on a Kafka cluster and vice-versa.

**Adding/Deleting edge nodes**

You can add an existing HDInsight cluster's empty edge node to a new cluster when you create the cluster. For more information, see [Use empty edge nodes on Apache Hadoop clusters in HDInsight](https://docs.microsoft.com/azure/hdinsight/hdinsight-apps-use-edge-node).

**Connecting HDInsight to your on-premise network**

If your error description contains **HostName Resolution failed**, this error points to a problem with the custom DNS configuration. DNS servers within a virtual network, can forward DNS queries to Azure’s recursive resolvers, to resolve host names within that virtual network. See [Name Resolution in Virtual Networks](https://docs.microsoft.com/azure/virtual-network/virtual-networks-name-resolution-for-vms-and-role-instances) for details.

Access to Azure’s recursive resolvers is provided via the virtual IP **168.63.129.16**. This IP is only accessible from the Azure Virtual Machines (VMs). The IP will not work if you are using an OnPrem DNS server, or your DNS server is an Azure VM which is not part of the cluster’s vNet.

For the steps to resolve this issue, see [ErrorDescription contains 'HostName Resolution failed'](https://hdinsight.github.io/ClusterCRUD/hdinsight-vnet#1-errordescription-contains-hostname-resolution-failed).

**HDInsight does not use private dns zone names for cluster setup**

You must create and configure the DNS server before installing HDInsight in the virtual network. For more information see [Create custom DNS server](https://docs.microsoft.com/azure/hdinsight/connect-on-premises-network#create-custom-dns-server)

**Additional Information**

If you are having technical issues with cluster creation, select **Create** instead of **Other Customization**. Also, if you are running into issues while trying to scale a cluster, please select **Scale** instead of **Other Customization**. Both **Create** and **Scale** will provide better solutions and applicable diagnostics.
## **Recommended Documents**
* [Azure HDInsight: Frequently asked questions](https://docs.microsoft.com/azure/hdinsight/hdinsight-faq)
* [Create Cluster Error Dictionary](https://docs.microsoft.com/azure/hdinsight/create-cluster-error-dictionary)

