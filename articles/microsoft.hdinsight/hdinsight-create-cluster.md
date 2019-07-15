<properties
    pageTitle="Create HDInsight Cluster"
    description="Common root causes for cluster creation issues"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="jaserano, v-miegge"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32636444"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
    articleId="hdinsight-create-cluster"
/>

# Create HDInsight Cluster

## **Recommended Steps**

Common root causes for cluster creation issues:

* Permissions issues

  * If you are using ADLS Gen 2, ensure that the user-assigned managed identity assigned to HDInsight cluster is in either the Storage Blob Data Contributor role, or the [Storage Blob Data Owner Role](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-use-data-lake-storage-gen2#set-up-permissions-for-the-managed-identity-on-the-data-lake-storage-gen2-account)<br>
  * If you are using [ADLS Gen 1](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-use-data-lake-store), understand that **ADLS Gen 1**  is not supported for HBASE clusters, and is not supported in HDI version 4.0<br>
  * If you are using Azure Storage, ensure that the storage account name is valid during the cluster creation

* A subscription-based Azure policy is in place, denying the creation of public IPs. HDInsight cluster creation requires two public IPs.

    The following policies often impact cluster creation:

  * Policies preventing the creation of IP Address & Load balancers within the subscription<br>
  * Policy preventing the creation of a storage account<br>
  * Policy preventing the deletion of networking resources (IP Address /Load Balancers)

* The customer has a firewall on their VNET, and Storage accounts rules which deny traffic

  * You must always allow traffic from the following IP addresses:

    * 168.61.49.99
    * 23.99.5.239
    * 168.61.48.131
    * 138.91.141.162

  * These IP addresses Destination must be set at **\*:433** and a Direction of "Inbound"<br>
  * If your cluster is in a specific region, add the respective source IP, which is listed in the following [link](https://docs.microsoft.com/azure/hdinsight/hdinsight-extend-hadoop-virtual-network#hdinsight-ip)<br>
  * If you are using either Express Route or your own custom DNS server, please follow [this link](https://docs.microsoft.com/azure/hdinsight/hdinsight-extend-hadoop-virtual-network#multinet)

* Resources have locks which impact cluster creation

  * Please ensure that there are no [locks on your VNET or Resource Group](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources)

* The customer is using an unsupported version of HDI and/or Apache Hadoop Component

  * Please ensure that you are using a [supported HDI version](https://docs.microsoft.com/azure/hdinsight/hdinsight-component-versioning#supported-hdinsight-versions) AND [Apache Hadoop Component version](https://docs.microsoft.com/azure/hdinsight/hdinsight-component-versioning#apache-hadoop-components-available-with-different-hdinsight-versions)

* The Storage Account name is violating Storage Account name restrictions

  * Storage Account names cannot be more than 24 characters and Storage account name cannot contain a special character. These restrictions also apply to the default container name in the storage account.

* A service outage

  * Check [Azure Status](https://status.azure.com/status) for any potential outages or service issues

## **Recommended Documents**

* [Extend Azure HDInsight using an Azure Virtual Network](https://docs.microsoft.com/azure/hdinsight/hdinsight-extend-hadoop-virtual-network)<br>
* [Use Azure Data Lake Storage Gen2 with Azure HDInsight clusters](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-use-data-lake-storage-gen2)<br>
* [Use Azure storage with Azure HDInsight clusters](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-use-blob-storage)<br>
* [Set up clusters in HDInsight with Apache Hadoop, Apache Spark, Apache Kafka, and more](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-provision-linux-clusters)
