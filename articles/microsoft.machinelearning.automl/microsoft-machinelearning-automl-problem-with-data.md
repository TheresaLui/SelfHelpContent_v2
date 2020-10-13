<properties
	pageTitle="Problem with data"
	description="Problem with data"
	infoBubbleText="Problem with data"
	service="microsoft.machinelearning.automl"
	resource="automl"
	authors="Aniththa"
	ms.author="anumamah"
	supportTopicIds="32755241"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.automl.problemwithdata"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem with data

In this article, you learn how to resolve automated machine learning related data.

Automated machine learning supports data that resides on your local desktop or in the cloud such as Azure Blob Storage. The data can be read into a Pandas DataFrame or an Azure Machine Learning TabularDataset. [Learn more about datasets](https://docs.microsoft.com/azure/machine-learning/how-to-create-register-datasets).

Requirements for training data:

* Data must be in tabular form
* The value to predict, target column, must be in the data

For remote experiments, training data must be accessible from the remote compute. AutoML only accepts [Azure Machine Learning TabularDatasets](https://docs.microsoft.com/python/api/azureml-core/azureml.data.tabulardataset?view=azure-ml-py&preserve-view=true) when working on a remote compute.

Azure Machine Learning datasets expose functionality to:

* Easily transfer data from static files or URL sources into your workspace
* Make your data available to training scripts when running on cloud compute resources. See [How to train with datasets](https://docs.microsoft.com/azure/machine-learning/how-to-train-with-datasets#mount-files-to-remote-compute-targets) for an example of using the Dataset class to mount data to your remote compute target.

## **Recommended Documents**

* [Data source and format](https://docs.microsoft.com/azure/machine-learning/how-to-configure-auto-train#data-source-and-format)
* [Featurization in automated machine learning](https://docs.microsoft.com/azure/machine-learning/how-to-configure-auto-features)
* [Forecasting with large data](https://github.com/microsoft/solution-accelerator-many-models)
* [Configure data splits and cross-validation in automated machine learning](https://docs.microsoft.com/azure/machine-learning/how-to-configure-cross-validation-data-splits)
* [Known Issues and Troubleshooting](https://docs.microsoft.com/azure/machine-learning/resource-known-issues#automated-machine-learning)
