<properties
	pageTitle="Can’t delete my files"
	description="Can’t delete my files"
	infoBubbleText="Can’t delete my files"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="abeomor"
	ms.author="osomorog"
	supportTopicIds="32739644"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.notebooks"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Can’t delete my files

If you can't delete a file, your compute instance may have a lock on that file. Most users are able to resolve their deleting file issue by using the following steps.

## **Recommended Steps**
1. Click "Compute" in the Azure ML Studio menu bar
2. On the compute page locate the Compute Instance with the issues
3. Restart the Compute Instance from here
4. After restarting the compute, try to delete the file again

## **Recommended Documents**

If you are experiencing issues with Studio Notebooks, here is a list of resources which may be helpful:
* [How to run Jupyter Notebooks in your workspace](https://docs.microsoft.com/azure/machine-learning/how-to-run-jupyter-notebooks)
* [Clone Git repositories into your workspace file system](https://docs.microsoft.com/azure/machine-learning/concept-train-model-git-integration#clone-git-repositories-into-your-workspace-file-system)
* [What is an Azure Machine Learning compute instance?](https://docs.microsoft.com/azure/machine-learning/concept-compute-instance)
