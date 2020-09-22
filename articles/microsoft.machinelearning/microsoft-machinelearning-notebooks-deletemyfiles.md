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
	articleId="microsoft.machinelearning.notebooks-deletemyfiles"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Can’t delete my files

If you can't delete a file/folder, your compute instance may have a lock on that file/folder or your file/folder is marked as read-only. Most users are able to resolve their deleting file/folder issues by using the following steps to change the permissions of the file/folder.

## **Recommended Steps**

1. Click the Terminal icon in the Notebook Toolbar
2. Go to the parent folder in the terminal with `cd ~/cloudfiles/code/Users/<user_name>`
3. Use `chmod -R 755 <folder_name>` command to change the permission on the folder or file
4. Try to delete the file/folder again

## **Recommended Documents**

* [How to run Jupyter Notebooks in your workspace](https://docs.microsoft.com/azure/machine-learning/how-to-run-jupyter-notebooks)
* [Clone Git repositories into your workspace file system](https://docs.microsoft.com/azure/machine-learning/concept-train-model-git-integration#clone-git-repositories-into-your-workspace-file-system)
* [What is an Azure Machine Learning compute instance?](https://docs.microsoft.com/azure/machine-learning/concept-compute-instance)
