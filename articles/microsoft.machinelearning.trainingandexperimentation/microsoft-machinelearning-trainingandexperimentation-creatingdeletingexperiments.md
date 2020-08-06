<properties
	pageTitle="Unable to create or delete an experiment"
	description="Unable to create or delete an experiment"
	infoBubbleText="Unable to create or delete an experiment"
	service="microsoft.machinelearning"
	resource="trainingandexperimentation"
	authors="mx-iao"
	ms.author="minxia"
	supportTopicIds="32690887"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.trainingandexperimentation.creatingdeletingexperiments"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Unable to create or delete an experiment
## **Recommended Steps**
### Experiment creation
When creating an experiment, you must provide an experiment name. The name must be 3-36 characters, start with a letter or a number, and can only contain letters, numbers, underscores, and dashes. For more information, see [here](https://docs.microsoft.com/python/api/azureml-core/azureml.core.experiment.experiment?view=azure-ml-py).

### Experiment deletion
Permanent deletion of experiments or runs is currently not supported in Azure ML. Archiving of experiments is supported. For more information, see [here](https://docs.microsoft.com/azure/machine-learning/resource-known-issues#run-or-experiment-deletion).

## **Recommended Documents**
If you are experiencing any issues with creating experiments, here is a list of additional resources which may be helpful:
* [Concept overview of Azure Machine Learning experiments](https://docs.microsoft.com/azure/machine-learning/concept-azure-machine-learning-architecture#experiments)
* [SDK reference documentation for the Experiment class](https://docs.microsoft.com/python/api/azureml-core/azureml.core.experiment.experiment?view=azure-ml-py)
