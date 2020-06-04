<properties
	pageTitle="Using a built-in pipeline step"
	description="Using a built-in pipeline step"
	infoBubbleText="Using a built-in pipeline step"
	service="microsoft.machinelearning"
	resource="pipelines"
	authors="bradwall"
	ms.author="bradwall"
	supportTopicIds="32690897"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.pipelines.usingpipelinestep"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Using a Built-In Pipeline Step

In this article, you will learn how to use built-in pipeline steps. Azure ML Pipelines provides a base PipelineStep class in the Python SDK, from which many other built-in step classes derive. See below for a list of currently supported pipeline step types.


## **Recommended Documents**

* [PipelineStep base class - Python SDK](https://docs.microsoft.com/python/api/azureml-pipeline-core/azureml.pipeline.core.builder.pipelinestep?view=azure-ml-py)
* [Running U-SQL scripts on Azure Data Lake Analytics with AdlaStep -Python SDK](https://docs.microsoft.com/python/api/azureml-pipeline-steps/azureml.pipeline.steps.adlastep?view=azure-ml-py)
* [Running Azure Batch jobs with AzureBatchStep - Python SDK](https://docs.microsoft.com/python/api/azureml-pipeline-steps/azureml.pipeline.steps.azurebatchstep?view=azure-ml-py)
* [Running DataBricks notebooks, Python script, or JAR jobs with DatabricksStep - Python SDK](https://docs.microsoft.com/python/api/azureml-pipeline-steps/azureml.pipeline.steps.databricksstep?view=azure-ml-py)
* [Transfer data between storages with DataTransferStep - Python SDK](https://docs.microsoft.com/python/api/azureml-pipeline-steps/azureml.pipeline.steps.datatransferstep?view=azure-ml-py)
* [Running Estimator for ML model training with EstimatorStep -Python SDK](https://docs.microsoft.com/python/api/azureml-pipeline-steps/azureml.pipeline.steps.estimatorstep?view=azure-ml-py)
* [Running hyperparameter tuning for ML model training - Python SDK](https://docs.microsoft.com/python/api/azureml-pipeline-steps/azureml.pipeline.steps.hyperdrivestep?view=azure-ml-py)
* [Run an Azure ML pipeline Module with ModuleStep -Python SDK](https://docs.microsoft.com/python/api/azureml-pipeline-steps/azureml.pipeline.steps.modulestep?view=azure-ml-py)
* [Run an MPI job with MPIStep - Python SDK](https://docs.microsoft.com/python/api/azureml-pipeline-steps/azureml.pipeline.steps.mpistep?view=azure-ml-py)
* [Run a Python script job with PythonScriptStep - Python SDK](https://docs.microsoft.com/python/api/azureml-pipeline-steps/azureml.pipeline.steps.pythonscriptstep?view=azure-ml-py)
* [Run an R script job with RScriptStep - Python SDK](https://docs.microsoft.com/python/api/azureml-pipeline-steps/azureml.pipeline.steps.rscriptstep?view=azure-ml-py)
