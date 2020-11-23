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
By creating a dataset, you create a reference to the data source location, along with a copy of its metadata. Because the data remains in its existing location, you incur no extra storage cost. You can create both TabularDataset and FileDataset data sets by using the Python SDK or through the [Azure Machine Learning studio](https://ml.azure.com).
For the data to be accessible by Azure Machine Learning, datasets must be created from paths in Azure datastores or public web URLs.

You can learn how to create or register an Azure Machine Learning datasets by using the following steps.

## **Recommended Steps**

1. Create [datastores](https://docs.microsoft.com/azure/machine-learning/how-to-access-data) to connect to your Azure storage service. We support Azure Blob storage, Azure Files, Azure Data Lake Storage Gen1, Azure Data Lake Storage Gen2, Azure SQL Database, and Azure Database for PostgreSQL.
2. Create [datasets](https://docs.microsoft.com/azure/machine-learning/how-to-create-register-datasets) from paths from your datastores

### **FAQ**

• **"Permission" problems reigistreing dataset or connecting to datastore

 If you have "Permission" problems reigistreing dataset or connecting to datastore, please find possible causes and steps to be taken as below:
1. **Network issues**: Please verify if you are facing issues with your network
2. **VNet issues**: Check if your data storage is behind a Vnet or firewall. If so, you must make sure your [Storage's Vnet setting is correct](https://docs.microsoft.com/azure/machine-learning/how-to-secure-workspace-vnet#secure-azure-storage-accounts).
3. **Incorrect credentials**: Verify if the credentials provided (SAS token or account key) for the datastore is correct and still active. If you are using ADLS Gen2, check out their access control set up to learn more: [access control set up for ADLS Gen 2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-access-control).
4. **Data deletion**: Verify if the data you are trying to access was deleted from the storage account
5. **FileNotExist error**: If you get similar error message as "cannot open file '/xxx/yyy/zzz.tsv': No such file or directory", please make sure the directory you are using exists



• **When should I use file dataset v/s tabular dataset?**
For majority of your use-cases, we recommend using file dataset for any file formats (csv, parquet, json, and so on) for ease of use. If you are using autoML and data monitors, then a tabular dataset helps you setting the filtering and partition once and reuse across autoML and data monitor components in Azure ML. Tabular dataset also provides data in table format and offers seamless options to move to pandas dataframe without creating a local copy of your data.

• **When should I use dataset mounting v/s datastore mounting?**
You should always use the dataset mount, upload and download options to benefit from the improved capabilities and advanced optimizations. [Learn more](https://docs.microsoft.com/azure/machine-learning/how-to-train-with-datasets#mount-files-to-remote-compute-targets). 

• **When should I use dataset upload/download v/s datastore upload/download?**
You should always use the dataset upload and download options to benefit from the improved capabilities and performance. [Learn more](https://docs.microsoft.com/azure/machine-learning/how-to-train-with-datasets#mount-vs-download). 

• **My data is in Azure SQL DW or SQL DB, how should I access data from AML workspace? What about on-premise SQL?**
Azure SQL DW: we do not recommend creating a datastore for SQL DW because the Azure ML datastore cannot perform parallel reads from your SQL DW, and you may encounter time out issues if your query has many filters. We recommend copying data to storages such as Blob or ADLS gen2 to register as datastore in Azure ML. 

Azure SQL DB: You can [create a dataset from SQLDB datastore](https://docs.microsoft.com/python/api/azureml-core/azureml.data.dataset_factory.tabulardatasetfactory?view=azure-ml-py#from-sql-query-query--validate-true--set-column-types-none--query-timeout-30-). To write back to SQL DB, you can either use [data transfer](https://docs.microsoft.com/python/api/azureml-pipeline-steps/azureml.pipeline.steps.datatransferstep?view=azure-ml-py) step in AzureML pipeline, or connect to SQL server in your script using [storage API](https://docs.microsoft.com/azure/azure-sql/database/connect-query-python?tabs=windows). 

On-premises SQL: if you do want to leverage on-premises SQL server directly, you can use Python pyodbc. [Learn more](https://pypi.org/project/pyodbc/).

• **Can I use ADLS gen2 as default storage for my workspace?**
Currently, ADLS Gen2 cannot be set as default storage for your workspace. When you create an Azure ML workspace, an Azure blob container named `workspaceblobstore` is created as default storage to store workspace artifacts and your machine learning experiment logs. You can choose to set this default storage as a blob storage of your choice by using the command `ws.set_default_datastore(new_default_datastore)`. See [this example](https://docs.microsoft.com/azure/machine-learning/how-to-access-data#get-datastores-from-your-workspace).

**Note:** You can still use ADLS Gen2 storage type when you create your own datastore in Azure ML for your training data, but not as a default datastore for your workspace artifacts and experiment logs.

### **Known Issues**
Learn about [known issues concerning AML working with data](https://docs.microsoft.com/azure/machine-learning/resource-known-issues#work-with-data)

## **Recommended Documents**

* [How to connect to Azure storage services](https://docs.microsoft.com/azure/machine-learning/how-to-access-data)
* [Cloud storage types being supported by Azure ML data stores](https://docs.microsoft.com/azure/machine-learning/concept-data#datastores)
* [How to create or register datasets](https://docs.microsoft.com/azure/machine-learning/how-to-create-register-datasets)
