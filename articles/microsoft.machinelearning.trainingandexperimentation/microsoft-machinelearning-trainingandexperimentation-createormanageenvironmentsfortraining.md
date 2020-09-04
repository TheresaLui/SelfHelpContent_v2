<properties
	pageTitle="Create or manage environments for training"
	description="Create or manage environments for training"
	infoBubbleText="Create or manage environments for training"
	service="microsoft.machinelearning"
	resource="trainingandexperimentation"
	authors="saachigopal"
	ms.author="sagopal"
	supportTopicIds="32690887"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.trainingandexperimentation.createormanageenvironments"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Issues creating or managing environments for training

## **Recommended Steps**
### Environment creation
Make sure to not start your own environment name with the AzureML prefix as it is reserved for curated environments. 

### Environment management
For issues with dependencies, remember to enable user_managed_dependencies if you want to disable the default Conda environment.

## **Recommended Documents**
If you are experiencing any issues with creating or managing environments, here is a list of additional resources which may be helpful:
* [How to use environments](https://docs.microsoft.com/azure/machine-learning/how-to-use-environments)
* [Concept overview](https://docs.microsoft.com/azure/machine-learning/concept-environments)
* [SDK documentation](https://docs.microsoft.com/python/api/azureml-core/azureml.core.environment)
