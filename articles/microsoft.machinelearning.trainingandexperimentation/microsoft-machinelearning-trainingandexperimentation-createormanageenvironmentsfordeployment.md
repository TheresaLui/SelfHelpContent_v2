<properties
	pageTitle="Create or manage environments for deployment"
	description="Create or manage environments for deployment"
	infoBubbleText="Create or manage environments for deployment"
	service="microsoft.machinelearning"
	resource="trainingandexperimentation"
	authors="saachigopal"
	ms.author="sagopal"
	supportTopicIds="32690848"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.trainingandexperimentation.createormanageenvironments"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Issues creating or managing environments for deployment

## **Recommended Steps**
### Environment creation
Make sure to not start your own environment name with the AzureML prefix as it is reserved for curated environments. 

### Environment management
For issues with dependencies, remember to enable user_managed_dependencies if you want to disable the default Conda environment.

## **Recommended Documents**
If you are experiencing any issues with creating or managing environments, here is a list of additional resources which may be helpful:
* [Deploy models with Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-and-where)
* [Deploy a model with a custom Docker image](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-custom-docker-image)
* [How to use environments](https://docs.microsoft.com/azure/machine-learning/how-to-use-environments)
* [SDK documentation](https://docs.microsoft.com/python/api/azureml-core/azureml.core.environment)

