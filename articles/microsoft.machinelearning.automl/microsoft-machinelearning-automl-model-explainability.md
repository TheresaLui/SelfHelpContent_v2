<properties
	pageTitle="Problem with model explainability"
	description="Problem with model explainability"
	infoBubbleText="Problem with model explainability"
	service="microsoft.machinelearning.automl"
	resource="automl"
	authors="Aniththa"
	ms.author="anumamah"
	supportTopicIds="32755242"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.automl.modelexplainability"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem with model explainability

In this article, you learn how to resolve automated machine learning related model explainability.

All SDK versions after 1.0.85 set model_explainability=True by default. 
In SDK version 1.0.85 and earlier versions users need to set model_explainability=True in the AutoMLConfig object in order to use model interpretability.

## **Recommended Documents**

* [Interpretability: model explanations in automated machine learning (preview)](https://docs.microsoft.com/azure/machine-learning/how-to-machine-learning-interpretability-automl)
* [Model interpretability in Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/how-to-machine-learning-interpretability)
* [Known Issues and Troubleshooting](https://docs.microsoft.com/azure/machine-learning/resource-known-issues#automated-machine-learning)
