<properties
	pageTitle="Problem accessing run details and logs"
	description="Problem accessing run details and logs"
	infoBubbleText="Problem accessing run details and logs"
	service="microsoft.machinelearning"
	resource="runs"
	authors="mx-iao"
	ms.author="minxia"
	supportTopicIds="32690885"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.runs.problemaccessingrundetailsandlogs"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem accessing run details and logs

Most users can resolve issues with accessing run details and logs by using the following information.

## **Recommended Steps**

### Monitoring and viewing ML run logs and metrics
Follow [these instructions](https://docs.microsoft.com/azure/machine-learning/how-to-monitor-view-training-logs) to learn how to add logging code to your training script, submit an experiment run, monitor that run, and inspect the results in Azure Machine Learning

### Unable to view logs
If you are unable to view your logs, check your workspace storage setting in the [Azure Portal](https://ms.portal.azure.com) to see if the ADLS Gen2 Hierarchical namespace (HNS) is enabled. You can check by navigating to your Storage Account, selecting the Configuration tab, and seeing if the Data Lake Storage Gen2 Hierarchical namespace is enabled or disabled. HNS is currently not supported by Azure Machine Learning, so you will need to create a new workspace with HNS disabled for your storage account. 

### Accessing run history from the UI
The training scripts, metrics, logs, outputs, and metadata of a training run are encapsulated in the run's history. To access the run history from the Azure Machine Learning studio client, navigate to the Experiment tab view and click the corresponding experiment. You can then access each of the runs in that experiment from the list view.

### Accessing run history from the SDK
Alternatively, you can access artifacts and contents of the run history by using the methods available on the [Run](https://docs.microsoft.com/python/api/azureml-core/azureml.core.run.run?view=azure-ml-py) class, such as `get_details_with_logs()`, `get_metrics()`, and `download_files()`.

### Accessing the code snapshot from run history
When a run is submitted, Azure Machine Learning compresses the source directory that contains the source code for the run as a zip file and stores the zip file as a [snapshot](https://docs.microsoft.com/azure/machine-learning/concept-azure-machine-learning-architecture#snapshots) as part of the run's history. To access a run's snapshot, use the [`get_snapshot_id()`](https://docs.microsoft.com/python/api/azureml-core/azureml.core.run.run?view=azure-ml-py#get-snapshot-id-) method. Then, call [`restore_snapshot()`](https://docs.microsoft.com/python/api/azureml-core/azureml.core.run.run?view=azure-ml-py#restore-snapshot-snapshot-id-none--path-none-) with the snapshot ID to download the zip file of the snapshot.

If there are files in the source directory that you do not want included in the run's snapshot, create either a `.gitignore` file or a `.amlignore` file, and specify the filename in the filenames to ignore. Learn more about [snapshot architecture](https://docs.microsoft.com/azure/machine-learning/concept-azure-machine-learning-architecture#snapshots).
