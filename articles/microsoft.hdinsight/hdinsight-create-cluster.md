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
    cloudEnvironments="public, Fairfax, usnat, ussec, mooncake, blackforest"
    articleId="hdinsight-create-cluster"
	ownershipId="AzureData_HDInsight"
/>

# Create HDInsight Cluster

## **Recommended Steps**

**Potential intermittent or transient issues**

Some errors are transient and your request may succeed if you retry creation after 15 minutes of the failed attempt. If after retrying your request, you still receive an error and are not able to address the issue, note the time frame in which the error occurred and file a support request in a timely manner. By providing a time frame and filing a support ticket within a few days of an event, support is more likely to be able to review logs to determine the root cause of the error as logs are only available for a specific amount of time.

**Azure portal error when creating a cluster with a public key**

When trying to create an Azure HDInsight cluster from the Azure portal and using an SSH authentication type of public key, users are experiencing an error when they click **Review + Create**. The error in the portal is "Must not contain any three consecutive characters from SSH username." This issue is being addressed; however, if you experience this issue, the workaround is to return to the **Create HDInsight cluster** blade in the portal, check the **Use cluster login password for SSH** box, and then uncheck the **Use cluster login password for SSH** box, and then click **Review + Create** again. Cluster creation should complete without error. 

**Issues with A2 VMs**

1. **Error:** VM size *A2 VM* provided in the request is invalid or not supported for role *node type*. Valid values are: *list of supported VMs*

1. **Cause:** A2-series virtual machines cannot be used as headnodes for ESP clusters due to not having enough capacity for handling Apache Ranger and other security related resource consumptions. Existing clusters with A2-series virtual machines used as headnodes can still be working and scaled up or down, or have edge nodes added to them.

1. **Solution:** Select a virtual machine from the list of supported VMs in the error message. 

**Error: Conflict (HTTP Status Code: 409)**

Cause: You deleted a cluster and are attempting to recreate it with the same name before the delete operation completed.

Solution: After deleting a cluster or encountering this error, wait 30-60 minutes before recreating a cluster with the same name.

**Error: interaction_required**

Cause: The conditional access or multi-factor authentication (MFA) policy is being applied to the user. Since interactive authentication is not supported yet, the user or the cluster needs to be exempted from the conditional access or MFA policies. If you choose to exempt the cluster (by using  an IP address based exemption policy), then make sure that the Active Directory service endpoints are enabled for that Virtual Network (VNet).

Solution: Use a conditional access policy and exempt the HDInsight clusters from MFA. For more information, see [interaction_required](https://docs.microsoft.com/azure/hdinsight/domain-joined/domain-joined-authentication-issues#interaction_required).

**Error: HiveMetastoreSchemaInitializationFailedErrorCode**

Solution: If you are using a custom Hive metastore, please run 'Hive Schema Tool' against your metastore to check for possible issues with metastore configuration. Also Check if Azure services or subnet is whitelisted in sql server firewall.

**A service outage**

* Check [Azure Status](https://status.azure.com/status) for any potential outages or service issues.

**Invalid Network Configuration**

* Due to having an invalid network configuration, the Azure AD Domain Services Sync Agent cannot reach customer's domain on TCP\443. This will cause cluster deployment failures.
* Solution:  [Follow Documentation](https://docs.microsoft.com/azure/active-directory-domain-services/synchronization).

**Azure Data Lake Storage Gen 1 and HBASE**

* If you are using [Azure Data Lake Storage Gen1](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-use-data-lake-store), understand that it is not supported for HBASE clusters, and is not supported in HDInsight version 4.0

**The customer is using an unsupported version of HDInsight and/or an Apache Hadoop Component**

* Ensure that you are using a [supported version of HDInsight](https://docs.microsoft.com/azure/hdinsight/hdinsight-component-versioning#supported-hdinsight-versions) AND a supported [Apache Hadoop Component version](https://docs.microsoft.com/azure/hdinsight/hdinsight-component-versioning#apache-hadoop-components-available-with-different-hdinsight-versions).

**The Storage account name is violating Storage account name restrictions**

* Storage account names cannot be more than 24 characters, must use numbers and lowercase letters only, and cannot contain special characters. These restrictions also apply to the default container name in the Storage account. For more information, see [Resolve errors for storage account names](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-storage-account-name-errors).


## **Recommended Documents**

* [Create Cluster Error Dictionary](https://docs.microsoft.com/azure/hdinsight/create-cluster-error-dictionary)
* [Custom Script Actions Troubleshooting](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-customize-cluster-linux#troubleshooting)
* [Creating or Deleting HDInsight Clusters FAQ](https://docs.microsoft.com/azure/hdinsight/hdinsight-faq#creating-or-deleting-hdinsight-clusters)
* [Extend Azure HDInsight using an Azure Virtual Network](https://docs.microsoft.com/azure/hdinsight/hdinsight-extend-hadoop-virtual-network)<br>
* [Use Azure Data Lake Storage Gen2 with Azure HDInsight clusters](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-use-data-lake-storage-gen2)<br>
* [Use Azure storage with Azure HDInsight clusters](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-use-blob-storage)<br>
* [Set up clusters in HDInsight with Apache Hadoop, Apache Spark, Apache Kafka, and more](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-provision-linux-clusters)
