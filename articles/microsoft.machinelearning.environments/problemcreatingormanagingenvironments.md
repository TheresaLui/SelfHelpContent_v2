<properties
	pageTitle="Problem creating or managing environments"
	description="Problem creating or managing environments"
	infoBubbleText="Problem creating or managing environments"
	service="microsoft.machinelearning"
	resource="environments"
	authors="saachigopal"
	ms.author="sagopal"
	supportTopicIds="32690887"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.environments.problemcreatingormanagingenvironments"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem creating or managing environments

## **Recommended Steps**
### Environment creation
The environment object defines the Python environment where experimentation will happen. AzureML Environment is usually defined by two parts (layers): system and Python layer. The system layer is defined by a base docker image or a user specified custom dockerfile. The python layer is a conda environment that is created from user specified python dependencies.

### Environment management
AzureML supports user managed environments that could be prefered by advanced users for complete control of the execution environment. With this scenario, the python layer will not be created. You can use a default docker image offered by Microsoft or build an image from specified base dockerfile.
To specify a user managed environment, please set user_managed_dependencies=True.

## **Recommended Documents**
If you are experiencing any issues with creating or managing environments, here is a list of additional resources which may be helpful:
* [How to use environments](https://docs.microsoft.com/azure/machine-learning/how-to-use-environments)
* [How to train models with PyTorch](https://docs.microsoft.com/azure/machine-learning/how-to-train-pytorch)
* [How to train models with TensorFlow](https://docs.microsoft.com/azure/machine-learning/how-to-train-tensorflow)
* [Concept overview](https://docs.microsoft.com/azure/machine-learning/concept-environments)
* [SDK documentation](https://docs.microsoft.com/python/api/azureml-core/azureml.core.environment)
