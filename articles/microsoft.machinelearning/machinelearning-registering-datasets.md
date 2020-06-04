<properties 
    pageTitle="Creating or registering datasets"
    description="Creating or registering datasets"
    service="microsoft.machinelearning"
    resource="dataset"
    authors="SturgeonMi"
    ms.author="xunwan"
    selfHelpType="generic"
    supportTopicIds="32690849"
    resourceTags=""
    productPesIds="16644"
    cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
 	articleId="machinelearning-registering-datasets"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Create or register Azure Machine Learning datasets
By creating a dataset, you create a reference to the data source location, along with a copy of its metadata. Because the data remains in its existing location, you incur no extra storage cost. You can create both TabularDataset and FileDataset data sets by using the Python SDK or the Azure Machine Learning studio at https://ml.azure.com.
For the data to be accessible by Azure Machine Learning, datasets must be created from paths in Azure datastores or public web URLs.

You can learn how to create or register an Azure Machine Learning datasets via documents below.

## **Recommended Steps**
1. Create datastores to connect to your Azure storage service. We support Azure Blob storage, Azure Files, Azure Data Lake Storage Gen1, Azure Data Lake Storage Gen2, Azure SQL Database, and Azure Database for PostgreSQL. [Learn how to create datastores](https://docs.microsoft.com/azure/machine-learning/how-to-access-data)
2. Create datasets from paths from your datastores. [Learn how to create datasets](https://docs.microsoft.com/azure/machine-learning/how-to-create-register-datasets)

## **Recommended Documents**
* [How to connect to Azure storage services](https://docs.microsoft.com/azure/machine-learning/how-to-access-data)
* [How to create or register datasets](https://docs.microsoft.com/azure/machine-learning/how-to-create-register-datasets)<br>
