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

Most users can resolve issues regarding managing runs and experiments by following the information below.

## **Recommended Documents**

### Start, monitor, or cancel runs
For information on starting and cancelling runs and monitoring run performance, see:

* [Start, monitor, and cancel training runs](https://docs.microsoft.com/azure/machine-learning/how-to-manage-runs?tabs=python) documentation
* [Manage runs](https://github.com/Azure/MachineLearningNotebooks/blob/master/how-to-use-azureml/track-and-monitor-experiments/manage-runs/manage-runs.ipynb) sample notebook

### Create and submit child runs
Creating child runs is supported in the SDK. For more information, see [Create child runs](https://docs.microsoft.com/azure/machine-learning/how-to-manage-runs?tabs=python#create-child-runs).

### Runs or experiment deletion
You can archive experiments by using the `Experiment.archive` method, or from the Experiment tab view in Azure Machine Learning studio client via the **Archive experiment** button. Archiving an experiment hides the experiment from list queries and views, but does not delete it.

Permanent deletion of individual experiments or runs is not currently supported. For more information on deleting workspace assets, see [Export or delete your Machine Learning service workspace data](https://docs.microsoft.com/azure/machine-learning/how-to-export-delete-data).
