<properties 
	pageTitle="Unable to complete the cluster create operation" 
	description="Error while provisioning an on-demand HDInsight cluster: Unable to complete the cluster create operation.. Error code: 400" 
	service="microsoft.datafactory" 
    resource="datafactories"
    authors="spelluru"
    displayOrder="6"
    selfHelpType="resource"
    cloudEnvironments="public"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
/>

# Unable to complete the cluster create operation with error code 400
You may see this error when provisioning an on-demand HDInsight cluster fails. 

## **Recommended steps**
When using a linked service of type **HDInsightOnDemand**, you need to specify a linkedServiceName that points to an Azure Blob Storage. Data Factory service uses this storage to store logs and supporting files for your on-demand HDInsight cluster.  Sometimes provisioning of an on-demand HDInsight cluster fails with the following error:

"Failed to create cluster. Exception: Unable to complete the cluster create operation. Operation failed with code '400'. Cluster left behind state: 'Error'. Message: 'StorageAccountNotColocated'."

This error usually indicates that the location of the storage account specified in the linkedServiceName is not in the same data center location where the HDInsight provisioning is happening. For example, if your Azure Data Factory location is West US, and the on-demand HDInsight provisioning happens in West US, but the Azure blob storage account location  is set to East US, the on-demand provisioning will fail.

Additionally, there is a second JSON property additionalLinkedServiceNames where additional storage accounts may be specified in on-demand HDInsight. Those additional linked storage accounts should be in the same location as the HDInsight cluster, or it will fail with the same error.

## **Recommended documents**
[HDInsight on-demand linked service](https://docs.microsoft.com/azure/data-factory/v1/data-factory-compute-linked-services#azure-hdinsight-on-demand-linked-service)