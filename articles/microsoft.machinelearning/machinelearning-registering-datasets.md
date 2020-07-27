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
1. Create datastores to connect to your Azure storage service. 

We support Azure Blob storage, Azure Files, Azure Data Lake Storage Gen1, Azure Data Lake Storage Gen2, Azure SQL Database, and Azure Database for PostgreSQL. [Learn how to create datastores](https://docs.microsoft.com/azure/machine-learning/how-to-access-data)

2. Create datasets from paths from your datastores.

[Learn how to create datasets](https://docs.microsoft.com/azure/machine-learning/how-to-create-register-datasets)

3. When should I use file dataset v/s tabular dataset?

For majority of your use-cases, we recommend using file dataset for any file formats (csv, parquet, json etc.) for ease of use. If you are using autoML and data monitors, then a tabular dataset helps you setting the filtering and partition once and reuse across autoML and data monitor components in Azure ML. Tabular dataset also provides data in table format and offers seamless options to move to pandas dataframe without creating a local copy of your data.

4. When should I use dataset mounting v/s datastore mounting?

You should always use the dataset mount, upload and download options to benefit from the improved capabilities and advanced optimizations.  Refer to this documentation for 
[details](https://docs.microsoft.com/azure/machine-learning/how-to-train-with-datasets#mount-files-to-remote-compute-targets). 

**Note**: Currently dataset mount has a known performance issue when working with millions of small files for small size of data (in MBs), until this issue is resolved, we recommend using datastore mount only for this scenario.

5. When should I use dataset upload/download v/s datastore upload/download?

You should always use the dataset upload and download options to benefit from the improved capabilities and performance.  Refer to this documentation for [details](https://docs.microsoft.com/azure/machine-learning/how-to-train-with-datasets#mount-vs-download). 


6. My data is in SQL DW, how should I access data from AML workspace? 

Creating a datastore for SQL DW is not recommended as Azure ML datastore cannot perform parallel reads from your SQL DW and you may encounter time out issues if your query has many filters. The recommended approach is to copy data to storages such as Blob or ADLS gen2 to register as datastore in Azure ML. 
 
7. Can I use ADLS gen2 as default storage for my workspace? 

No, currently ADLS Gen2 cannot be set as default storage for your workspace. When you create an Azure ML workspace, an Azure blob container named workspaceblobstore is created as default storage to store workspace artifacts and your machine learning experiment logs. You can choose to set this default storage as a blob storage of your choice by using the command : ws.set_default_datastore(new_default_datastore). Please refer to an example [here](https://docs.microsoft.com/azure/machine-learning/how-to-access-data#get-datastores-from-your-workspace).

**Note**: You can still use ADLS Gen2 storage type when you create your own datastore in Azure ML for your training data, but not as a default datastore for your workspace artifacts and experiment logs.


## **Recommended Documents**
* [How to connect to Azure storage services](https://docs.microsoft.com/azure/machine-learning/how-to-access-data)
* [How to create or register datasets](https://docs.microsoft.com/azure/machine-learning/how-to-create-register-datasets)<br>




