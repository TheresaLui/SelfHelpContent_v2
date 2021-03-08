<properties
	pageTitle="Pipeline run fails"
	description="Running Azure ML pipelines"
	infoBubbleText="Running Azure ML pipelines"
	service="microsoft.machinelearning"
	resource="pipelines"
	authors="shbijlan"
	ms.author="shbijlan"
	supportTopicIds="32690881"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.pipelines.runningpipelines"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Submitting and running pipelines

In this article, you will learn how to submit, run, and debug Azure ML pipelines.

### **Common Issues**
Problem with cache and reuse
* Only upload files relevant to the job at hand. Any change in files within the data directory will be seen as reason to rerun the step the next time the pipeline is run even if reuse is specified.

Performing management operations on compute targets
* This is not supported from inside remote jobs. Since machine learning pipelines are submitted as a remote job, do not use management operations on compute targets from inside the pipeline.

Unable to pass data to PipelineData directory
* Ensure you have created a directory in the script that corresponds to where your pipeline expects the step output data. In most cases, an input argument will define the output directory, and then you create the directory explicitly. Use os.makedirs(args.output_dir, exist_ok=True) to create the output directory. See the tutorial for a scoring script example that shows this design pattern.

Dependency bugs
* If you see dependency errors in your remote pipeline that did not occur when locally testing, confirm your remote environment dependencies and versions match those in your test environment. See [Environment building, caching, and reuse](https://docs.microsoft.com/azure/machine-learning/concept-environments#environment-building-caching-and-reuse)



## **Recommended Documents**

* [How to submit a pipeline - Python SDK](https://docs.microsoft.com/azure/machine-learning/how-to-create-your-first-pipeline#submit-the-pipeline)
* [Some notes about caching and reuse](https://docs.microsoft.com/azure/machine-learning/how-to-create-your-first-pipeline#caching--reuse)
* [Running a published pipeline - Python SDK](https://docs.microsoft.com/azure/machine-learning/how-to-create-your-first-pipeline#run-a-published-pipeline)
* [Submitting a job to a pipeline endpoint - Python SDK](https://docs.microsoft.com/azure/machine-learning/how-to-create-your-first-pipeline#submit-a-job-to-a-pipeline-endpoint)
* [Debug and troubleshoot machine learning pipelines](https://docs.microsoft.com/azure/machine-learning/how-to-debug-pipelines)
* [Debug and troubleshoot ParallelRunStep](https://docs.microsoft.com/azure/machine-learning/how-to-debug-parallel-run-step)

