<properties
    pageTitle="HDInsight cluster with Azure Active Directory integration"
    description="Azure Active Directory integration"
    service="microsoft.HDInsight"
    resource="clusters"
    authors="TobyTu"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32636438"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="d51bcaf5-bec9-4e83-a49b-fde2d1d43229"
	ownershipId="AzureData_HDInsight"
/>

# HDInsight with Azure Active Directory integration

## **Recommended Steps**

**Errors: FailedToJoinDomain, DomainNotFoundInActiveDirectory or ActiveDirectoryAuthenticationFailed**

See [Troubleshooting HDInsight cluster deployment issue due to the domain join fails](https://github.com/HDInsight/HDInsight.github.io/blob/master/EnterpriseSecurityPackage/DomainJoinIssues.md).
 
**Error: SecureHadoopWaitForOuContainerCreationActivityTimedOut**

This error may occur because too many operations are in progress. To resolve the issue, reduce the amount of currently running operations and then retry.

**Error: FailedToConnectWithClusterErrorCode**
 
If you use network security groups or user defined routes to control inbound traffic to your HDInsight cluster, you must ensure that your cluster can communicate with critical Azure health and management services. For more information, see [HDInsight management IP addresses](https://docs.microsoft.com/azure/HDInsight/HDInsight-management-ip-addresses).

**Certificate Issues**

Make sure that your SSL Certificate is not expired.For more information, see [Refresh the HDInsight certificate for Data Lake Storage Gen1 access](https://docs.microsoft.com/azure/HDInsight/HDInsight-hadoop-use-data-lake-store#refresh-the-HDInsight-certificate-for-data-lake-storage-gen1-access).

**Permissions**

Only tenant administrators have the privileges to enable Azure Active Directory Domain Service. If the cluster storage is Azure Data Lake Storage Gen1 or Gen2, you must disable Multi-Factor Authentication (MFA) only for users who will need to access the cluster using basic Kerberos authentications.

You can use trusted IP addresses or Conditional Access to disable MFA for specific users when they are accessing the HDInsight cluster virtual network IP range. If you are using Conditional Access, make sure that AD service endpoint in enabled on the HDInsight virtual network. If the cluster storage is Azure Blob Storage, do not disable MFA.

**Invalid Network Configuration**

* Due to having an invalid network configuration, the Azure AD Domain Services Sync Agent cannot reach customer's domain on TCP\443. This will cause cluster deployment failures.
* Solution:  [Follow Documentation](https://docs.microsoft.com/azure/active-directory-domain-services/synchronization)

**Additional Information**

- Azure Active Directory Domain Service must be deployed in an Azure Resource Manager based virtual network. Classic virtual networks are not supported for Azure Active Directory Domain Service. For more information, see [Networking considerations](https://docs.microsoft.com/azure/HDInsight/domain-joined/apache-domain-joined-configure-using-azure-adds#networking-considerations).
- Enterprise Security Package (ESP) is generally available in HDInsight 3.6 and 4.0 for cluster types: Apache Spark, Interactive, Apache Hadoop and HBase. ESP for Apache Kafka cluster type is currently in preview.

## **Recommended Documents**

* [Create Cluster Error Dictionary](https://docs.microsoft.com/azure/hdinsight/create-cluster-error-dictionary)
* [APACHE domain joined configure using Azure ADDS](https://docs.microsoft.com/azure/HDInsight/domain-joined/apache-domain-joined-configure-using-azure-adds)
* [Check if HDInsight VNET is peered to AAD-DS VNET](https://docs.microsoft.com/azure/HDInsight/domain-joined/apache-domain-joined-configure-using-azure-adds#networking-considerations)
* [Check if secure LDAP is configured correctly with the right certificate](https://docs.microsoft.com/azure/HDInsight/domain-joined/apache-domain-joined-configure-using-azure-adds#enable-azure-ad-ds)
* [Make sure the managed identity has the right role assigned to it](https://docs.microsoft.com/azure/HDInsight/domain-joined/apache-domain-joined-configure-using-azure-adds#create-and-authorize-a-managed-identity)
