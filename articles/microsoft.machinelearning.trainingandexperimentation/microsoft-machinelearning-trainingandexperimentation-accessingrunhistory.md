<properties
	pageTitle="Issues with accessing run history"
	description="Issues with accessing run history"
	infoBubbleText="Issues with accessing run history"
	service="microsoft.machinelearning"
	resource="trainingandexperimentation"
	authors="mx-iao"
	ms.author="minxia"
	supportTopicIds="32690885"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.trainingandexperimentation.accessingrunhistory"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Issues with accessing run history

## **Recommended Steps**
### Accessing run history from the UI
An experiment run's training scripts, metrics, logs, outputs, and metadata are encapsulated in the run's history. To access the run history from the Azure Machine Learning studio client, navigate to the "Experiment" tab view and click on the corresponding experiment. Each of the runs in that experiment are then accessible from the list view.

### Accessing run history from the SDK
You can alternatively also access artifacts and contents of the run history using the methods available on the [Run](https://docs.microsoft.com/python/api/azureml-core/azureml.core.run.run?view=azure-ml-py) class, e.g. `get_details_with_logs()`, `get_metrics()`, `download_files()`.

### Accessing the code snapshot from run history
When a run is submitted, Azure Machine Learning compresses the source directory that contains the source code for the run as a zip file and stores the zip file as a [snapshot](https://docs.microsoft.com/azure/machine-learning/concept-azure-machine-learning-architecture#snapshots) as part of the run's history. To access a run's snapshot, use the [`get_snapshot_id()`](https://docs.microsoft.com/python/api/azureml-core/azureml.core.run.run?view=azure-ml-py#get-snapshot-id-) method. Then, call [`restore_snapshot()`](https://docs.microsoft.com/python/api/azureml-core/azureml.core.run.run?view=azure-ml-py#restore-snapshot-snapshot-id-none--path-none-) with the snapshot ID to download the zip file of the snapshot.

If there are files in the source directory that you do not want included in the run's snapshot, make either a .gitignore or .amlignore file and specify in it the filenames to ignore. See [here](https://docs.microsoft.com/azure/machine-learning/concept-azure-machine-learning-architecture#snapshots) for more information.
