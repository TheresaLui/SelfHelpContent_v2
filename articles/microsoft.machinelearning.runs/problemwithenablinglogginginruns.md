<properties
	pageTitle="Problem with enabling logging in runs"
	description="Problem with enabling logging in runs"
	infoBubbleText="Problem with enabling logging in runs"
	service="microsoft.machinelearning"
	resource="runs"
	authors="mx-iao"
	ms.author="minxia"
	supportTopicIds="32755222"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.runs.problemwithenablinglogginginruns"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem with enabling logging in runs

Most users are able to resolve issues with enabling logging in runs by using the following information.

## **Recommended Steps**

### Using the Azure ML SDK for logging
For interactive logging and logging metrics in remote runs using the Azure ML logging APIs, see [Enable logging in Azure ML training runs](https://docs.microsoft.com/azure/machine-learning/how-to-track-experiments).

#### Metric document is too large
Azure Machine Learning has internal limits on the size of metric objects that can be logged at once from a training run. If you encounter a "Metric Document is too large" error when logging a list-valued metric, try splitting the list into smaller chunks, for example:

```
run.log_list("my metric name", my_metric[:N])
run.log_list("my metric name", my_metric[N:])
```

Internally, Azure ML concatenates the blocks with the same metric name into a contiguous list.

### Using TensorBoard
If you want to use TensorBoard to visualize the metrics of your training runs, see [Visualize experiment runs and metrics with TensorBoard](https://docs.microsoft.com/azure/machine-learning/how-to-monitor-tensorboard).

### Using MLFlow
For information on using MLFlow's tracking API to log metrics in your training runs, see [Track experiment runs with MLFlow](https://docs.microsoft.com/azure/machine-learning/how-to-use-mlflow).
