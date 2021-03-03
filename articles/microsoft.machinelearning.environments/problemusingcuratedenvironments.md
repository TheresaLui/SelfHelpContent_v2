<properties
	pageTitle="Problem using curated environments"
	description="Problem using curated environments"
	infoBubbleText="Problem using curated environments"
	service="microsoft.machinelearning"
	resource="environments"
	authors="saachigopal"
	ms.author="sagopal"
	supportTopicIds="32755204"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.environments.problemusingcuratedenvironments"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem using curated environments

## **Recommended Steps**
### Environment creation
Make sure to not start your own environment name with the AzureML or Microsoft prefix as it is reserved for curated environments. In addition, if you modify the curated environment object and submit an experiment with it, the same issue will arise.

### Modifying curated environments
If you want to modify a curated environment, make sure to clone and rename: `Environment.get(workspace=ws, name="AzureML-Minimal").clone(new_name)`. Now you are free to make any changes as you would with a custom environment.

## **Recommended Documents**
If you are experiencing any issues with curated environments, here is a list of additional resources which may be helpful:
* [Curated environments](https://docs.microsoft.com/azure/machine-learning/resource-curated-environments)
* [How to use environments](https://docs.microsoft.com/azure/machine-learning/how-to-use-environments#create-an-environment)
* [Concept overview](https://docs.microsoft.com/azure/machine-learning/concept-environments)
* [SDK documentation](https://docs.microsoft.com/python/api/azureml-core/azureml.core.environment)
