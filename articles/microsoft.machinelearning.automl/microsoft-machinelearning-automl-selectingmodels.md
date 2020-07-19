<properties
    pageTitle="Selecting models in Azure Automated ML"
    description="Select specific algorithms to be used or excluded in Azure Automated ML training"
    infoBubbleText="Selecting models in Azure Automated ML"
    service="microsoft.machinelearning.automl"
    resource="automl"
    authors="CESARDELATORRE"
    ms.author="cesardl"
    supportTopicIds="32690882"
    productPesIds="16644"
    cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
    articleId="microsoft-machinelearning-automl-selectingmodels.md"
    selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# How to select or block algorithms in Azure Automated ML

By default, when using AutoML and after specifying what ML problem/task you want to solve (such as `Regression`, `Classification` or `Forecast`) for your target model, AutoML will try all the possible algorithms available for that selected problem/task.

For further details on all the algorithms to be tried automatically by AutoML, you can review all of them in the article [Configure automated ML experiments in Python - Select your experiment type](https://docs.microsoft.com/azure/machine-learning/how-to-configure-auto-train#select-your-experiment-type).

However, once you have tried multiple experiment runs for your particular dataset you might know that you want to discard certain algorithms that don't offer good results (blacklist algorithms). Or vice-versa, you might know that you only want to try a limited number of algorithms (whitelist algorithms). For those cases, here are the steps you can follow in order to select or block specific algorithms.

There are two possible ways of doing this action with AutoML:
* AutoML Python SDK
* AutoML UI (User Interface)

## **Recommended Steps using AutoML Python SDK**

1. Locate your AutoMLConfig class such as the following code with a simple AutoML configuration:
	```
	from azureml.train.automl import AutoMLConfig

	# task can be one of classification, regression, forecasting
	automl_config = AutoMLConfig(task = "classification",
								 training_data = train_dataset,
								 label_column_name = "Age")
	```
2. If you want to whitelist algorithms, meaning to select and use only certain algorithms, add that list to the `whitelist_models` parameter like in the following code:
	```
	from azureml.train.automl import AutoMLConfig

	# task can be one of classification, regression, forecasting
	automl_config = AutoMLConfig(task = "classification",
								 training_data = train_dataset,
								 label_column_name = "Age",
								 whitelist_models=['LightGBM','SVM','LogisticRegression']
								 )
	```
This code basically means that AutoML child runs will only use the algorithms `LightGBM`, `SVM`, `LogisticRegression` while trying multiple combinations of hyper-parameters in the multiple child runs to be tried.

3. If you want to blacklist a list algorithms, meaning to only block certain algorithms and try the rest of algorithms availabe in AutoML, add that list to the `blacklist_models` parameter like in the following code:
	```
	from azureml.train.automl import AutoMLConfig

	# task can be one of classification, regression, forecasting
	automl_config = AutoMLConfig(task = "classification",
								 training_data = train_dataset,
								 label_column_name = "Age",
								 blacklist_models=['DecisionTree','BernoulliNaiveBayes']
								 )
	```
This code basically means that AutoML child runs will try all the available algorithms in AutoML targeting the `classification` problem. only use the algorithms `LightGBM`, `SVM`, `LogisticRegression` while trying multiple combinations of hyper-parameters in the multiple child runs to be tried.

4. Note that usually you will either whitelist or blacklist algorithms. It doesn't make much sense to use both at the same time.

5. In order to find out the names of all the possible algorithms supported by AutoML (constants or name IDs to be provided in your code), consult that in the following AutoML SDK reference pages:

	* [Names/Constants of Classification algorithms](https://docs.microsoft.com/python/api/azureml-train-automl-client/azureml.train.automl.constants.supportedmodels.classification?view=azure-ml-py)
	* [Names/Constants of Regression algorithms](https://docs.microsoft.com/python/api/azureml-train-automl-client/azureml.train.automl.constants.supportedmodels.regression?view=azure-ml-py)
	* [Names/Constants of Time Series Forecast algorithms](https://docs.microsoft.com/python/api/azureml-train-automl-client/azureml.train.automl.constants.supportedmodels.forecasting?view=azure-ml-py)


## **Recommended Steps using AutoML UI (In Azure Machine Learning studio UI)**

You can also discard algorithms when creating an experiment in the Automated ML UI. 

Note that when using the UI you currently cannot whitelist algorithms, only blacklist algorithms.

1. Create a new Automated run.

2. On the 'Task type and settings' form (where you select the task type such as classification, regression, or forecasting), click on the 'View additional configuration settings' link and in the 'Blocked algorithm' select the algorithms you want to exclude/block from the training job.

## **Recommended Documents**

* [Configure automated ML experiments in Python](https://docs.microsoft.com/azure/machine-learning/how-to-configure-auto-train)
* [Create, explore, and deploy automated machine learning experiments with Azure ML UI](https://docs.microsoft.com/azure/machine-learning/how-to-create-portal-experiments)
