<properties
	pageTitle="Accessing or registering Open Datasets"
	description="Accessing or registering Open Datasets"
	infoBubbleText="Accessing or registering Open Datasets"
	service="microsoft.machinelearning"
	resource="opendatasets"
	authors="rsavage2"
	ms.author="rasavage"
	selfHelpType="generic"
	supportTopicIds="32690833"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
  articleId="open-datasets-accessingandregisteringdatasets"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Azure Open Datasets: Accessing or registering Open Datasets

With an Azure account, you can access open datasets using code or through the Azure service interface. The data is colocated with Azure cloud compute resources for use in your machine learning solution.
Open Datasets are available through the Azure Machine Learning UI and SDK. Open Datasets also provides Azure Notebooks and Azure Databricks notebooks you can use to connect data to Azure Machine Learning and Azure Databricks. Datasets can also be accessed through a Python SDK.
However, you don't need an Azure account to access Open Datasets; you can access them from any Python environment with or without Spark.

## **Recommended Steps**

1. Locate the azureml.opendatasets class that corresponds to the desired [azureml open dataset](https://docs.microsoft.com/python/api/azureml-opendatasets/azureml.opendatasets?view=azure-ml-py)
2. This is an example of code for accessing and registering open datasets:

```
from azureml.opendatasets import [Dataset class]

data = [Daataset class].get_tabular_dataset()

```

or

```
from azureml.opendatasets import [Dataset class]

data = [Daataset class].get_file_dataset()

```

## **Recommended Documents**

* [Open Datasets Packages and Classes](https://docs.microsoft.com/python/api/azureml-opendatasets/azureml.opendatasets?view=azure-ml-py)
* [What are Azure Open Datasets](https://docs.microsoft.com/azure/open-datasets/overview-what-are-open-datasets#access-to-datasets)
* [Azure Open Datasets Catalog](https://azure.microsoft.com/services/open-datasets/catalog/)
