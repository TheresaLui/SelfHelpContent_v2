<properties
	pageTitle="Can’t access Notebook shared with me by URL"
	description="Can’t access Notebook shared with me by URL"
	infoBubbleText="Can’t access Notebook shared with me by URL"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="abeomor"
	ms.author="osomorog"
	supportTopicIds="32739643"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.notebooks"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Can’t access Notebook shared with me by URL

To view shared Notebooks you have to have access to the workspace. Most users are able to resolve their Notebook access issue by asking the user that sent the link to follow the follwing steps.

## **Recommended Steps**
1. Make sure the user you sent the link to has access to your workspace
2. Go to [Access control](data-blade:Microsoft.MachineLearningServices.Access-control-(IAM)) on Azure Machine Learning workspace 
3. Check if the user you send the link to have access to your workspace.
4. If the user doesn't have access, Click the "+ Add" button
5. Add the user the approirate level of access. 

Note: Reader access is the minimum level of access to view a shared Notebook

## **Recommended Documents**

If you are experiencing issues with Studio Notebooks, here is a list of resources which may be helpful:
* [How to run Jupyter Notebooks in your workspace](https://docs.microsoft.com/azure/machine-learning/how-to-run-jupyter-notebooks)
* [Clone Git repositories into your workspace file system](https://docs.microsoft.com/azure/machine-learning/concept-train-model-git-integration#clone-git-repositories-into-your-workspace-file-system)
* [What is an Azure Machine Learning compute instance?](https://docs.microsoft.com/azure/machine-learning/concept-compute-instance)
