<properties
	pageTitle="Creating or Publishing an Azure ML Pipeline"
	description="Creating or Publishing an Azure ML Pipeline"
	infoBubbleText="Creating or Publishing an Azure ML Pipeline"
	service="microsoft.machinelearning"
	resource="pipelines"
	authors="bradwall"
	ms.author="bradwall"
	supportTopicIds="32690845"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.pipelines.createdeactivatepipeline"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Creating or Publishing an Azure ML Pipeline

Pipeline data

- Only upload files relevant to the job at hand. Any change in files within the data directory will be seen as reason to rerun the step the next time the pipeline is run, even if reuse is specified.
- To prevent unnecessary files from being included in the snapshot, create an ignore file (.gitignore or .amlignore) in the directory. Add the files and directories to exclude to this file.
- When you create a PipelineData object, you must provide a name and a datastore where the data will reside. Pass your `PipelineData` object(s) to your `PythonScriptStep` using both the arguments and the outputs arguments.
- Writing output data back to a datastore using PipelineData is supported only for Azure Blob and Azure File share datastores.
- To write output data back to Azure Blob, Azure File share, and ADLS Gen 1 and ADLS Gen 2 datastores, use the public preview class, `OutputFileDatasetConfig`.
- Within your pipeline's `PythonScriptStep`, you can retrieve the available output paths using the program's arguments. If this step is the first and will initialize the output data, you must create the directory at the specified path. You can then write whatever files you want to be contained in the PipelineData.

Roles and Permissions
- Performing management operations on compute targets is not supported from inside remote jobs. Since machine learning pipelines are submitted as a remote job, do not use management operations on compute targets from inside the pipeline.
- If you're using Azure role-based access control (Azure RBAC) to manage access to your pipeline, set the permissions for your pipeline scenario (training or scoring).

## **Recommended Documents**

* [Understand ML pipelines](https://docs.microsoft.com/azure/machine-learning/concept-ml-pipelines)
* [Create a pipeline with the Python SDK](https://docs.microsoft.com/azure/machine-learning/concept-ml-pipelines#building-pipelines-with-the-python-sdk)
* [Create a pipeline with the Python SDK, detailed](https://docs.microsoft.com/azure/machine-learning/how-to-create-your-first-pipeline)
* [Create a pipeline using the designer](https://docs.microsoft.com/azure/machine-learning/concept-ml-pipelines#building-pipelines-with-the-designer)
* [Deactivate or deprecate a pipeline](https://docs.microsoft.com/azure/machine-learning/how-to-schedule-pipelines#deactivate-the-pipeline)
* [How to debug pipelines](https://docs.microsoft.com/azure/machine-learning/how-to-debug-pipelines)
