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

## **Recommended Steps**

### ModuleError
If you are running into ModuleErrors (No module named), it means that the training script is expecting a package to be installed but it missing in the training environment. You will need to ensure that your Azure ML environment includes the missing dependency. See [Create and manage Azure ML environments](https://docs.microsoft.com/azure/machine-learning/how-to-use-environments) for more information.

### NameError (Name not defined), AttributeError (Object has no attribute)
This exception should come from your training script. You can look at the log files from the Azure ML studio UI to get more information about the specific name not defined or attribute error. From the SDK, you can use run.get_details() to look at the error message. This will also list all the log files generated for your run. Please make sure to take a look at your training script and fix the error before resubmitting your run.

### ImportError: No module named ruamel.yaml
This issue is encountered with the installation of the Azure ML Python SDK on the latest pip (>20.1.1) in the conda base environment for all released versions of Azure Machine Learning SDK for Python. Refer to the following workarounds:

* Avoid installing the Python SDK on the conda base environment, rather create your conda environment and install SDK on that newly created user environment. The latest pip should work on that new conda environment.
* For creating custom Docker images, where you cannot switch away from conda base environment, please pin pip<=20.1.1 in the dockerfile.

### Image build failure
If your submitted job fails and the failure happens during the image build process, see the "Docker and Python Package Management > Environment build fails" support topic for suggestions on how to resolve.

### Horovod has been shut down
In most cases if you encounter "AbortedError: Horovod has been shut down" this exception means there was an underlying exception in one of the processes that caused Horovod to shut down. Each rank in the MPI job gets it own dedicated log file in Azure ML. These logs are named 70_driver_logs. In case of distributed training, the log names are suffixed with "_rank" to make it easier to differentiate the logs. To find the exact error that caused Horovod to shut down, go through all the log files and look for Traceback at the end of the driver_log files. One of these files will give you the actual underlying exception.
