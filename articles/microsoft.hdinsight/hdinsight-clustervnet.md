<properties
    pageTitle="Azure HDInsight: Virtual Network"
    description="Azure HDInsight: Virtual Network"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="TobyTu"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32636507"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, mooncake"
    articleId="bfa4e56c-3fbc-461d-a7d5-1e485b42932b"
/>

# Azure HDInsight: Virtual Network

## Cluster creation fails due to an issue with User-Defined Rules error codes: InvalidNetworkConfigurationErrorCode

Virtual Network configuration is not compatible with HDInsight Requirement. Error: 'Failed to connect to Azure Storage Account' or  'Failed to connect to Azure SQL'

## **Recommended Steps**

Please follow the steps listed in the [troubleshooting guide](https://hdinsight.github.io/ClusterCRUD/hdinsight-vnet#2-errordescription-contains-failed-to-connect-to-azure-storage-account-or-failed-to-connect-to-azure-sql) to make sure that your user defined rules are configured correctly.

## **Recommended Documents**

* [VNET and Networking](https://docs.microsoft.com/azure/hdinsight/hdinsight-extend-hadoop-virtual-network)
* [For ESP clusters, check if HDInsight VNET is peered to AAD-DS VNET](https://docs.microsoft.com/azure/hdinsight/domain-joined/apache-domain-joined-configure-using-azure-adds#networking-considerations)
