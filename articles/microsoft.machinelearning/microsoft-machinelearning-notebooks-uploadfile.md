<properties
	pageTitle="Can't upload a file"
	description="Can't upload a file"
	infoBubbleText="Can't upload a file"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="abeomor"
	ms.author="osomorog"
	supportTopicIds="32739647"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.notebooks-uploadfile"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Can't upload a file

Your file might be more than 95MB. Most users are able to resolve their Compute Instance issue by using the following steps.

## **Recommended Steps**
1. In the Azure Portal, search "Machine Learning" 
2. Click the "Machine Learning" service 
3. Find your workspace, and click your workspace name to open the Machine Learning Workspace blabe.
4. Go to "Overview"
2. Click the Storage Link to be redirect to your Storage account for your workspace.
3. Click "File Share" and select the file share with the prefix *code-*
4. Go into the Users folder.
5. This is the same directory as the File Explorer in Notebooks
6. Try to upload your files here.


## **Recommended Documents**

If you are experiencing issues with Studio Notebooks, here is a list of resources which may be helpful:
* [How to run Jupyter Notebooks in your workspace](https://docs.microsoft.com/azure/machine-learning/how-to-run-jupyter-notebooks)
* [Clone Git repositories into your workspace file system](https://docs.microsoft.com/azure/machine-learning/concept-train-model-git-integration#clone-git-repositories-into-your-workspace-file-system)

