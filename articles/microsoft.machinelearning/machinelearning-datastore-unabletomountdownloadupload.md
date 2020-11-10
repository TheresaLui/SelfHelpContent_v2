<properties
	pageTitle="Unable to mount, download, upload to a datastore"
	description="Unable to mount, download, upload to a datastore"
	service="microsoft.machinelearning"
	resource="datasets"
	authors="sihhu"
	ms.author="sihhu"
	selfHelpType="generic"
	supportTopicIds="32690891"
	resourceTags=""
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleid="machinelearning-datastore-unabletomountdownloadupload"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Unable to mount, download, upload to a datastore

After retrieving a datastore from the workspace, if you are unable to mount, download, or upload to the datastores, follow the steps below to diagnose and resolve the issue. 

## **Recommended Steps**

1. Check the type of your datastore. You can do so by running the following code:

```
datastore = workspace.datastores['YourDatastoreName']
print(datastore)
```

2. If your datastore type is Azure Data Lake, Azure Data Lake Gen 2
Azure SQL Database, Azure Database for PostgreSQL, Databricks File System, or Azure Database for MySQL, downloading, mounting and uploading are not supported. If your datastore type is Azure File Share, mounting is not supported. 
To download or mount data from Azure Blob, Azure File Share, Azure Data Lake, Azure Data Lake Gen 2, we recommend you to create an Azure Machine Learning dataset and use the dataset for data delivery. Learn [how to create datasets](https://docs.microsoft.com/azure/machine-learning/how-to-create-register-datasets) and [how to use datasets in training](https://docs.microsoft.com/azure/machine-learning/how-to-train-with-datasets).
3. Check whether credentials stored in your datastore is valid. To update the datastore credentials, you can either do it on Azure Machine Learning studio UI, or register the datastore using the same name via SDK. Learn [how to register datastore](https://docs.microsoft.com/azure/machine-learning/how-to-access-data).
4. Check whether your storage account is behind virtual network or firewall. If your storage account is behind vnet or firewall, you can only download, mount or upload data if your compute target is behind the same vnet or firewall. Learn more about [how to work with vnet](https://docs.microsoft.com/azure/machine-learning/how-to-enable-virtual-network).

## **Recommended Documents**

* [Access data in Azure storage services](https://docs.microsoft.com/azure/machine-learning/how-to-access-data)
* [Create Azure Machine Learning datasets](https://docs.microsoft.com/azure/machine-learning/how-to-create-register-datasets)
* [Train with datasets in Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/how-to-train-with-datasets)

