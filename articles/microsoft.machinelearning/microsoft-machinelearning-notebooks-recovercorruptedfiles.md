<properties
	pageTitle="Recover my deleted or corrupted files"
	description="Recover my deleted or corrupted files"
	infoBubbleText="Recover my deleted or corrupted files"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="abeomor"
	ms.author="osomorog"
	supportTopicIds="32739651"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.notebooks-recovercorrupted"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Recover my deleted or corrupted files

If your file was deleted or corrupted you might be able to find it in the checkpoints folder on your compute instance. Most users are able to resolve their corrupted file issue using the documentation below

## **Recommended Steps**
1. Open the Terminal.
2. Go into the folder that contains the corrupted file.
3. The checkpoint file is located within a hidden folder names .ipynb_checkpoints located with the same folder as the initial ipynb file.
4. Copy this file into a folder outside the .ipynb_checkpoints to view it.

## **Recommended Documents**

If you are experiencing issues with Studio Notebooks, here is a list of resources which may be helpful:
* [How to run Jupyter Notebooks in your workspace](https://docs.microsoft.com/azure/machine-learning/how-to-run-jupyter-notebooks)
* [Clone Git repositories into your workspace file system](https://docs.microsoft.com/azure/machine-learning/concept-train-model-git-integration#clone-git-repositories-into-your-workspace-file-system)
* [What is an Azure Machine Learning compute instance?](https://docs.microsoft.com/azure/machine-learning/concept-compute-instance)
