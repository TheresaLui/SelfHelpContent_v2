
<properties
    pageTitle="Problem with compute"
    description="Multiple options to submit experiments in Azure Automate ML"
    infoBubbleText="Problem with compute"
    service="microsoft.machinelearning.automl"
    resource="automl"
    authors="Aniththa"
    ms.author="anumamah"
    supportTopicIds="32755240"
    productPesIds="16644"
    cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
    articleId="microsoft-machinelearning-automl-problem-with-compute"
    selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>
# Problem with compute

In this article, you learn the multiple compute options you can use to train in Azure Automated Machine Learning.

An automated machine learning training experiment can run on the following compute options. Learn the [pros and cons of local and remote compute](https://docs.microsoft.com/azure/machine-learning/concept-automated-ml#local-remote) options.

* Your local machine such as a local desktop or laptop – Generally when you have a small dataset and you are still in the exploration stage. See [this notebook](https://github.com/Azure/MachineLearningNotebooks/blob/master/how-to-use-azureml/automated-machine-learning/local-run-classification-credit-card-fraud/auto-ml-classification-credit-card-fraud-local.ipynb) for a local compute example.
* A remote machine in the cloud – [Azure Machine Learning Managed Compute](https://docs.microsoft.com/azure/machine-learning/concept-compute-target#amlcompute) is a managed service that enables the ability to train machine learning models on clusters of Azure virtual machines. See [this notebook](https://github.com/Azure/MachineLearningNotebooks/blob/master/how-to-use-azureml/automated-machine-learning/classification-bank-marketing-all-features/auto-ml-classification-bank-marketing-all-features.ipynb) for a remote example using Azure Machine Learning Managed Compute.
* An Azure Databricks cluster in your Azure subscription. You can find more details here - [Setup Azure Databricks cluster for Automated ML](https://docs.microsoft.com/azure/machine-learning/how-to-configure-environment#aml-databricks). See [this GitHub site](https://github.com/Azure/MachineLearningNotebooks/tree/master/how-to-use-azureml/azure-databricks/automl) for examples of notebooks with Azure Databricks.



## **Recommended Documents**

* [Train models with automated machine learning in the cloud](https://docs.microsoft.com/azure/machine-learning/how-to-auto-train-remote)
* [What are compute targets in Azure Machine Learning?](https://docs.microsoft.com/azure/machine-learning/concept-compute-target)
* [Tutorial: Use automated machine learning to predict taxi fares](https://docs.microsoft.com/azure/machine-learning/tutorial-auto-train-models)
* [Configure automated ML experiments in Python](https://docs.microsoft.com/azure/machine-learning/how-to-configure-auto-train)
* [Create, explore, and deploy automated machine learning experiments with Azure ML UI](https://docs.microsoft.com/azure/machine-learning/how-to-use-automated-ml-for-ml-models)
* [Tutorial: Create your first classification model with automated machine learning](https://docs.microsoft.com/azure/machine-learning/tutorial-first-experiment-automated-ml)
