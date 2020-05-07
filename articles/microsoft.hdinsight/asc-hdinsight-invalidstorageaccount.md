<properties
    pageTitle="HDInsight Invalid Storage Account"
    description="HDInsightInvalidStorageAccount"
    infoBubbleText="Found recent invalid storage account. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="anirudhrege"
    ms.author="v-anreg"
    displayOrder=""
    articleId="Hdi_Crud_InvalidStorageAccount"
    diagnosticScenario="HDInsightInvalidStorageAccountInsight"
    selfHelpType="rca"
    supportTopicIds="32636423"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
There is a problem with the storage account required to create your HDInsight cluster. <br>
The storage account selected does not support page blobs which is a requirement for this cluster type.
<!--/issueDescription-->

## **Recommended Steps**

1. Select the account kind as Storage(general purpose) instead of BlobStorage while creating a storage account.
2. Select the storage account you created while configuring your HDInsight cluster.
