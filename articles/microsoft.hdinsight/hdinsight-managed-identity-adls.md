<properties
    pageTitle="Managed Identity"
    description="Managed Identity"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="v-miegge"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32636439"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="70e00cfb-358b-4f9d-9da9-c37d48c5a038"
	ownershipId="AzureData_HDInsight"
/>

# Managed Identity

**Permissions issues**

If you are using Azure Data Lake Storage Gen2 as the storage account for HDInsight cluster, ensure that the user assigned managed identity assigned to the HDInsight cluster is in either the Storage Blob Data Contributor role or the [Storage Blob Data Owner](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-use-data-lake-storage-gen2#set-up-permissions-for-the-managed-identity-on-the-data-lake-storage-gen2-account) for the Azure Data Lake Storage Gen2 storage account.

To assign the correct role:

1. Create an Azure storage account and enable Data Lake Storage Gen2 for the storage account
1. Create a user assigned managed identity
1. In the Storage accounts blade, add the user-assigned managed identity to either the Storage Blob Data Owner role, or the Storage Blob Data Contributor role, on the storage account
1. Proceed with cluster creation workflow

**Adding Secondary Azure Data Lake Storage Gen2**

To add a secondary Data Lake Storage Gen2 account, at the storage account level, assign the managed identity you have created, to the new Data Lake Storage Gen2 storage account that you wish to add.

**Note**: Adding a secondary Data Lake Storage Gen2 account via the **Additional storage accounts** blade on HDInsight is not supported. To add ADLS Gen 2 as a secondary storage account, you must use Azure CLI, Azure PowerShell, ARM template, or SDK.

**Adding Azure Data Lake Storage Gen2 to an existing cluster**

You cannot add Azure Data Lake Storage Gen2 as the storage account for HDInsight cluster account to an existing cluster. It must be configured during cluster creation.

**Firewall on Storage Account**

Verify that you have not enabled a Firewall on your Storage account that does not allow connections for the HDInsight VNET. Instructions for updating your Storage Firewall can be found at [Configure Azure Storage firewalls and virtual networks](https://docs.microsoft.com/azure/storage/common/storage-network-security).

**Creating Cluster with ADLS Gen2 through Azure CLI Template**

If you are creating a cluster with ADLS Gen2 through Azure CLI, use our [sample template](https://github.com/Azure-Samples/hdinsight-data-lake-storage-gen2-templates/blob/master/hdinsight-adls-gen2-template.json) and [sample parameters](https://github.com/Azure-Samples/hdinsight-data-lake-storage-gen2-templates/blob/master/hdinsight-adls-gen2-template.json) to ensure you are using proper syntax. For more information, see [Create a cluster with Data Lake Storage Gen2 through the Azure CLI](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-use-data-lake-storage-gen2#create-a-cluster-with-data-lake-storage-gen2-through-the-azure-cli).

## **Recommended Documents**

* [Use Azure Data Lake Storage Gen2 with Azure HDInsight clusters](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-use-data-lake-storage-gen2#use-the-azure-portal)
* [HDInsight storage FAQ](https://docs.microsoft.com/azure/hdinsight/hdinsight-faq#storage)
* [Create Cluster Error Dictionary](https://docs.microsoft.com/azure/hdinsight/create-cluster-error-dictionary)
