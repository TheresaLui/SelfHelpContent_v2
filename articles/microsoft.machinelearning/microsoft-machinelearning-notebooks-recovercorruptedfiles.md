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

If your file was deleted or corrupted you might be able to find it in the checkpoints folder on your compute instance. Most users are able to resolve their corrupted file issue using the steps below.

## **Recommended Steps**

1. Open the Terminal
2. Go into the folder that contains the corrupted file
3. The checkpoint file is located within a hidden folder names .ipynb_checkpoints located with the same folder as the initial ipynb file
4. Copy this file into a folder outside the .ipynb_checkpoints to view it
5. If you are still unable to recover your file from the checkpoints folder.
6. Head to the [Azure Portal](https://portal.azure.com/) and find your Azure Machine Learning Workspace resource in the Azure Portal
7. In the Machine Learning Workspace summary page in the Azure Portal, click the Storage Link and you will land in the Storage account associate with the workspace
8. In the Storage account page, find and click "File Share"
9. Find the container with the name that looks similar to "code-391ff5ac-6576-460f-ba4d-7e03433c68b6"
10. In the File Share Container you will be able to see all File Share snapshots in the menu on the left

## **Recommended Documents**

* [Overview of share snapshots for Azure Files](https://docs.microsoft.com/azure/storage/files/storage-snapshots-files)
* [How to run Jupyter Notebooks in your workspace](https://docs.microsoft.com/azure/machine-learning/how-to-run-jupyter-notebooks)
* [Clone Git repositories into your workspace file system](https://docs.microsoft.com/azure/machine-learning/concept-train-model-git-integration#clone-git-repositories-into-your-workspace-file-system)
