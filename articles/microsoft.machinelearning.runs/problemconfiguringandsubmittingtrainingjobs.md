<properties
	pageTitle="Problem configuring and submitting training jobs"
	description="Problem configuring and submitting training jobs"
	infoBubbleText="Problem configuring and submitting training jobs"
	service="microsoft.machinelearning"
	resource="runs"
	authors="mx-iao"
	ms.author="minxia"
	supportTopicIds="32690863"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.runs.problemconfiguringandsubmittingtrainingjobs"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem configuring and submitting training jobs

Most users can resolve issues regarding configuring and submitting training jobs by using the following information.

## **Recommended Steps**

### Configure training jobs

As of the Azure ML Python SDK 1.15.0 release, [ScriptRunConfig](https://docs.microsoft.com/python/api/azureml-core/azureml.core.scriptrunconfig?view=azure-ml-py) is the recommended method for configuring your training runs. If you are having issues configuring runs with Estimators, upgrade your SDK to >= 1.15.0 and use `ScriptRunConfig`. 

For more information and examples, see the following resources:

* [Configure and submit training runs](https://docs.microsoft.com/azure/machine-learning/how-to-set-up-training-targets)
* [Train with Scikit-learn](https://docs.microsoft.com/azure/machine-learning/how-to-train-scikit-learn)
* [Train with PyTorch](https://docs.microsoft.com/azure/machine-learning/how-to-train-pytorch)
* [Train with TensorFlow](https://docs.microsoft.com/azure/machine-learning/how-to-train-tensorflow)

### Configure distributed training jobs

TO configure distributed training jobs, see the following resources:

* [Reference architecture of distributed training of deep learning models in Azure ML](https://docs.microsoft.com/azure/architecture/reference-architectures/ai/training-deep-learning)
* [Distributed training with PyTorch](https://docs.microsoft.com/azure/machine-learning/how-to-train-pytorch#distributed-training)
* [Distributed training with TejsorFlow](https://docs.microsoft.com/azure/machine-learning/how-to-train-tensorflow#distributed-training)

### Write output files

For instructions on writing output files during training on remote compute so that they are persisted, see [where to save and write files for Azure ML experiments](https://docs.microsoft.com/azure/machine-learning/how-to-save-write-experiment-files#where-to-write-files).

### Resolve error messages regarding storage limits of code snapshots

Azure ML automatically takes a snapshot of your code based on the source_directory you specify when you configure the run. This snapshot has a total limit of 300 MB and/or 2000 files. 

If either limit is exceeded, you will see the following error when you submit your run:

```
While attempting to take snapshot of .
Your total snapshot size exceeds the limit of 300.0 MB
```

To resolve this, see [Storage limits of experiment snapshot](https://docs.microsoft.com/azure/machine-learning/how-to-save-write-experiment-files#storage-limits-of-experiment-snapshots).
