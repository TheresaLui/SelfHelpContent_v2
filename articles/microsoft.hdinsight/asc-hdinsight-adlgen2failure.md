<properties
    pageTitle="HDInsight Azure Data Lake Gen2 Failure"
    description="HDInsightAzureDataLakeGen2Failure"
    infoBubbleText="Found recent Azure Data Lake Gen2 Failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="anirudhrege"
    ms.author="v-anreg"
    displayOrder=""
    articleId="Hdi_Crud_AzureDataLakeGen2Failure"
    diagnosticScenario="HDInsightAzureDataLakeGen2FailureInsight"
    selfHelpType="rca"
    supportTopicIds="32636423, 32636439"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
There is a problem with the Azure Data Lake Gen2 account configured for your HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName-->. The Managed Service Identity (MSI) requires "Storage Blob Data Owner" permission.
<!--/issueDescription-->

## **Recommended Steps**

1. Create an Azure storage account and enable Data Lake Storage Gen 2 preview
2. Create a user assigned managed identity
3. Assign Storage Blob Data Owner access to the created managed identity on Azure Storage
4. In the Storage blade, select the Storage Account, and the associated managed user identity, and proceed with cluster creation workflow

## **Recommended Documents**

* [Azure HDInsight integration with Data Lake Storage Gen2](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-use-data-lake-storage-gen2#use-the-azure-portal)
* [Managed identities for Azure resources](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/overview)
