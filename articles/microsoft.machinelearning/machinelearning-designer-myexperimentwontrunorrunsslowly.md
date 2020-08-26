<properties
	pageTitle="My experiment won't run or runs slowly"
	description="My experiment won't run or runs slowly"
	infoBubbleText="My experiment won't run or runs slowly"
	service="microsoft.machinelearning"
	resource="designer"
	authors="likebupt"
	ms.author="keli19"
	displayOrder="1"
	articleId="machinelearning-designer-myexperimentwontrunorrunsslowly"
	selfHelpType="generic"
	supportTopicIds="32690867"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# My experiment won't run or runs slowly

Most users are able to resolve this issue using the steps below.

## **Recommended Steps**

1. Check if your compute target is warm. It may take several minutes to start from a cold compute. In Azure Machine Learning studio, click **Compute** -> **Training clusters** -> **[compute target name]** to check the compute status and details. On **Details** page, you can also change the **Idle seconds before scale down** to longer period (by default it’s 120 second) by clicking **Edit** button.
2. If you are running on a warm compute target, make sure the compute target has enough memory to handle the data size in your pipeline
3. If you have custom conda dependency and image, it will also lead to long environment preparation cost. You can check the azureml-logs of each module to see the time cost for image building and image download.
4. If your scheduled pipeline runs hang abnormally, file an issue by clicking the smiling face on top right corner of Azure Machine Learning studio and engineering team will investigate
5. You might also benefit from running Azure Machine Learning pipeline if there’s no change of the outputs in your previous modules. The system will auto-detect it and will not rerun the whole pipeline again (which should be much faster than your first time run).
6. You could also submit feedback by clicking the smiling face on top right corner of Azure Machine Learning studio with **including screenshot** checked on, better with **Microsoft can email ou about your feedback** checked on in case we need to follow up with you with your specific case

## **Recommended Documents**

* [What is Azure Machine Learning designer (preview)?](https://docs.microsoft.com/azure/machine-learning/concept-designer)
* [Debug and troubleshoot machine learning pipelines](https://docs.microsoft.com/azure/machine-learning/how-to-debug-pipelines)
