<properties
	pageTitle="Problem managing runs and experiments"
	description="Problem managing runs and experiments"
	infoBubbleText="Problem managing runs and experiments"
	service="microsoft.machinelearning"
	resource="runs"
	authors="mx-iao"
	ms.author="minxia"
	supportTopicIds="32755220"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.runs.problemmanagingrunsandexperiments"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem managing runs and experiments

## **Recommended Documents**

### Start, monitor, or cancel runs
For information on starting and cancelling runs and monitoring run performace, see:

* [Start, monitor, and cancel training runs](https://docs.microsoft.com/azure/machine-learning/how-to-manage-runs?tabs=python) documentation
* [Manage runs](https://github.com/Azure/MachineLearningNotebooks/blob/master/how-to-use-azureml/track-and-monitor-experiments/manage-runs/manage-runs.ipynb) sample notebook

### Create and submit child runs
Creation of child runs is supported in the SDK. See [Create child runs](https://docs.microsoft.com/azure/machine-learning/how-to-manage-runs?tabs=python#create-child-runs) for more information.

### Runs or experiment deletion
Experiments can be archived by using the Experiment.archive method, or from the Experiment tab view in Azure Machine Learning studio client via the "Archive experiment" button. This action hides the experiment from list queries and views, but does not delete it.

Permanent deletion of individual experiments or runs is not currently supported. For more information on deleting Workspace assets, see [Export or delete your Machine Learning service workspace data](https://docs.microsoft.com/azure/machine-learning/how-to-export-delete-data).
