<properties
	pageTitle="Remote run fails"
	description="Remote run fails"
	infoBubbleText="Remote run fails"
	service="microsoft.machinelearning"
	resource="runs"
	authors="mx-iao"
	ms.author="minxia"
	supportTopicIds="32690868"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.runs.remoterunfails"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Remote run fails

Most users are able to resolve issues with remote run fails by using the information below.

## **Recommended Steps**

### ModuleError
If you are running into ModuleErrors (no module named), it means that the training script is expecting a package to be installed, but the package missing in the training environment. You will need to ensure that your Azure ML environment includes the missing dependency. See [Create and manage Azure ML environments](https://docs.microsoft.com/azure/machine-learning/how-to-use-environments).

### NameError (name not defined), AttributeError (object has no attribute)
This exception probably comes from your training script. Review the log files from the Azure ML studio UI to get more information about the specific name not defined or the attribute error. From the SDK, you can use `run.get_details()` to view the error message. You'll also be able to see a list of all the log files generated for your run.

Make sure to take a look at your training script and fix the error before resubmitting your run.

### ImportError: No module named ruamel.yaml
You may see this error message when installing the Azure ML Python SDK on the latest pip (>20.1.1) in the conda base environment for all released versions of Azure Machine Learning SDK for Python. Use the following workarounds:

* Do not install the Python SDK on the conda base environment. Instead, create a new conda environment and install the Python SDK there.
* For creating custom Docker images where you cannot switch away from conda base environment, pin `pip<=20.1.1` in the dockerfile.

### Horovod has been shut down
If you receive an "AbortedError: Horovod has been shut down" error message, this means that there was an underlying exception in one of the processes that caused Horovod to shut down. Each rank in the MPI job gets it own dedicated log file in Azure ML. These logs are named `70_driver_logs`. In case of distributed training, the log names are suffixed with `_rank` to make it easier to differentiate the logs. To find the exact error that caused Horovod to shut down, review all the log files and look for Traceback at the end of the driver_log files. One of these files will give you the underlying exception.
