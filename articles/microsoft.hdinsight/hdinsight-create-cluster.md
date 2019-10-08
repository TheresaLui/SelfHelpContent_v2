<properties
    pageTitle="Create HDInsight Cluster"
    description="Common root causes for cluster creation issues"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="jaserano, v-miegge"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32681541"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
    articleId="hdinsight-create-cluster"
/>

# Create HDInsight Cluster

## **Recommended Steps**

**Potential intermittent or transient issuse**

*Some errors are transient and your request may succeed if you retry creation after 15 minutes of the failed attempt. If after retrying your request, you still receive an error and are not able to address the issue, note the timeframe in which the error occurred and file a support request in a timely manner. By providing a timeframe and filing a support ticket within a few days of an event, support is more likely to be able to review logs to determine the root cause of the error as logs are only available for a specific amount of time.

**Error: Conflict (HTTP Status Code: 409)**

Cause: You deleted a cluster and are attempting to recreate it with the same name before the operation completed.

Solution: After deleting a cluster or encountering this error, wait 30-60 minutes before recreating a cluster with the same name.

**Error: interaction_required**

Cause: The conditional access policy or MFA is being applied to the user. Since interactive authentication is not supported yet, the user or the cluster needs to be exempted from MFA / Conditional access. If you choose to exempt the cluster (IP address based exemption policy), then make sure that the AD ServiceEndpoints are enabled for that vnet.

Solution: Use conditional access policy and exempt the HDInisght clusters from MFA 

[More information common authentication issues in Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/domain-joined/domain-joined-authentication-issues#interaction_required)

### A service outage

* Check [Azure Status](https://status.azure.com/status) for any potential outages or service issues

**Azure Data Lake Storage Gen 1 and HBASE**

* If you are using [Azure Data Lake Storage Gen 1](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-use-data-lake-store), understand that it is not supported for HBASE clusters, and is not supported in HDI version 4.0

**The customer is using an unsupported version of HDI and/or Apache Hadoop Component**

* Please ensure that you are using a [supported HDI version](https://docs.microsoft.com/azure/hdinsight/hdinsight-component-versioning#supported-hdinsight-versions) AND [Apache Hadoop Component version](https://docs.microsoft.com/azure/hdinsight/hdinsight-component-versioning#apache-hadoop-components-available-with-different-hdinsight-versions)

**The Storage Account name is violating Storage Account name restrictions**

* Storage Account names cannot be more than 24 characters and Storage account name cannot contain a special character. These restrictions also apply to the default container name in the storage account.


## **Recommended Documents**

* [Creating or Deleting HDInsight Clusters FAQ](https://docs.microsoft.com/azure/hdinsight/hdinsight-faq#creating-or-deleting-hdinsight-clusters)
* [Extend Azure HDInsight using an Azure Virtual Network](https://docs.microsoft.com/azure/hdinsight/hdinsight-extend-hadoop-virtual-network)<br>
* [Use Azure Data Lake Storage Gen2 with Azure HDInsight clusters](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-use-data-lake-storage-gen2)<br>
* [Use Azure storage with Azure HDInsight clusters](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-use-blob-storage)<br>
* [Set up clusters in HDInsight with Apache Hadoop, Apache Spark, Apache Kafka, and more](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-provision-linux-clusters)
