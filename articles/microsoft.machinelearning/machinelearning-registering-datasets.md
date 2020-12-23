<properties
  pagetitle="Create or register Azure Machine Learning datasets&#xD;"
  service="microsoft.machinelearning"
  resource="dataset"
  ms.author="xunwan"
  selfhelptype="Generic"
  supporttopicids="32690849"
  resourcetags=""
  productpesids="16644"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="machinelearning-registering-datasets"
  ownershipid="AzureML_AzureMachineLearningServices" />
  
# Create or register Azure Machine Learning datasets

By creating a dataset, you create a reference to the data source location, along with a copy of its metadata. Because the data remains in its existing location, you incur no extra storage cost. You can create both TabularDataset and FileDataset data sets by using the Python SDK or through the [Azure Machine Learning studio](https://ml.azure.com).

For the data to be accessible by Azure Machine Learning, datasets must be created from paths in Azure datastores or public web URLs.

You can learn how to create or register an Azure Machine Learning datasets by using the following steps.

## **Recommended Steps**

1. Create [datastores](https://docs.microsoft.com/azure/machine-learning/how-to-access-data) to connect to your Azure storage service. We support Azure Blob storage, Azure Files, Azure Data Lake Storage Gen1, Azure Data Lake Storage Gen2, Azure SQL Database, and Azure Database for PostgreSQL.

2. Create [datasets](https://docs.microsoft.com/azure/machine-learning/how-to-create-register-datasets) from paths from your datastores

### **FAQ**

**Permission problems registering a dataset or connecting to datastore**

If you have Permission issues when registering dataset or connecting to datastore, do the following: 
* **Network issues**: Verify if you are facing issues with your network
* **VNet issues**: Check that your data storage is behind a Vnet or a firewall. If so, you must make sure that your [Storage's Vnet setting is correct](https://docs.microsoft.com/azure/machine-learning/how-to-secure-workspace-vnet#secure-azure-storage-accounts).
* **Incorrect credentials**: Verify that the credentials provided (SAS token or account key) for the datastore are correct and still active. If you are using ADLS Gen2, [check out their access control setup to learn more](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-access-control).
* **Data deletion**: Verify that the data you are trying to access was deleted from the storage account
* **FileNotExist error**: If you get an error message similar to "Cannot open file `/xxx/yyy/zzz.tsv` -  No such file or directory", verify  that the directory you are using exists


**When should I use a file dataset v/s a tabular dataset?**

For the majority of your use cases, we recommend using a file dataset for any file formats (csv, parquet, json, and so on). If you are using autoML and data monitors, then a tabular dataset helps you set the filtering and partition once and then reuse across autoML and data monitor components in Azure ML. Tabular dataset also provides data in table format and offers seamless options to move to pandas dataframe without creating a local copy of your data.

**When should I use dataset mounting v/s datastore mounting?**
   
You should always use the dataset mount, upload, and download options to benefit from the improved capabilities and advanced optimizations. [Learn more](https://docs.microsoft.com/azure/machine-learning/how-to-train-with-datasets#mount-files-to-remote-compute-targets). 

**When should I use dataset upload/download v/s datastore upload/download?**

You should always use the dataset upload and download options to benefit from the improved capabilities and performance. [Learn more](https://docs.microsoft.com/azure/machine-learning/how-to-train-with-datasets#mount-vs-download). 


**My data is in Azure SQL DW or SQL DB, how should I access data from AML workspace? What about on-premise SQL?**
   
* **Azure SQL DW:** We don't recommend creating a datastore for Azure SQL DW. The Azure ML datastore cannot perform parallel reads from your SQL DW and may encounter time-out issues if your query has many filters. We recommend copying data to storages, such as Blob or ADLS gen2, to register as a datastore in Azure ML. 

* **Azure SQL DB:** You can [create a dataset from SQLDB datastore](https://docs.microsoft.com/python/api/azureml-core/azureml.data.dataset_factory.tabulardatasetfactory?view=azure-ml-py#from-sql-query-query--validate-true--set-column-types-none--query-timeout-30-). To write back to SQL DB, either use the [data transfer](https://docs.microsoft.com/python/api/azureml-pipeline-steps/azureml.pipeline.steps.datatransferstep?view=azure-ml-py) step in AzureML pipeline, or connect to SQL server in your script using [storage API](https://docs.microsoft.com/azure/azure-sql/database/connect-query-python?tabs=windows). 

* **On-premises SQL:** To leverage on-premises SQL server directly, use Python pyodbc. [Learn more](https://pypi.org/project/pyodbc/).



**Can I use ADLS gen2 as the default storage for my workspace?**

Currently, ADLS Gen2 cannot be set as default storage for your workspace. When you create an Azure ML workspace, an Azure blob container named `workspaceblobstore` is created as default storage to store workspace artifacts and your machine learning experiment logs. You can choose to set this default storage as a blob storage of your choice by using the command `ws.set_default_datastore(new_default_datastore)`. See [this example](https://docs.microsoft.com/azure/machine-learning/how-to-access-data#get-datastores-from-your-workspace).

**Note:** You can still use ADLS Gen2 storage type when you create your own datastore in Azure ML for your training data, but not as a default datastore for your workspace artifacts and experiment logs.



### **Known Issues**
Learn about [known issues concerning AML working with data](https://docs.microsoft.com/azure/machine-learning/resource-known-issues#work-with-data)



## **Recommended Documents**

* [How to connect to Azure storage services](https://docs.microsoft.com/azure/machine-learning/how-to-access-data)
* [Cloud storage types being supported by Azure ML data stores](https://docs.microsoft.com/azure/machine-learning/concept-data#datastores)
* [How to create or register datasets](https://docs.microsoft.com/azure/machine-learning/how-to-create-register-datasets)
